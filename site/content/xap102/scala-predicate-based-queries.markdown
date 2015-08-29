---
layout: post102
title:  Predicate Based Queries
categories: XAP102
parent: scala.html
weight: 300
---


{{% summary  %}}{{% /summary %}}

Support for predicate based queries on the `GigaSpace` proxy has been in added. This support is based on the new macros feature introduced in Scala 2.10.  Each predicate based query is transformed during compilation into an equivalent [SQLQuery](./query-sql.html).


# Usage

To use predicate based queries, import `import org.openspaces.scala.core.ScalaGigaSpacesImplicits._` into scope. Then call the `predicate` method on the `GigaSpace` instance as demonstrated:

{{% highlight scala %}}
/* Import GigaSpace implicits into scope */
import org.openspaces.scala.core.ScalaGigaSpacesImplicits._

/* implicit conversion on gigaspace returns a wrapper class with predicate based query methods */
val predicateGigaSpace = gigaSpace.predicate
{{% /highlight %}}

# Supported Queries

## Example data class

For the purpose of demonstration, we will use the following example data class

{{% highlight scala %}}
case class Person @SpaceClassConstructor() (

  @BeanProperty
  @SpaceId
  id: String = null,

  @BeanProperty
  name: String = null,

  @BeanProperty
  @SpaceProperty(nullValue = "-1")
  @SpaceIndex(`type` = SpaceIndexType.EXTENDED)
  height: Int = -1,

  @BeanProperty
  birthday: Date = null,

  @BeanProperty
  son: Person = null

)
{{% /highlight %}}

## Translations

{: .table .table-bordered}
|Predicate Query|Translated SQL Query|
|:--------------|:-------------------|
|`==` <br> predicateGigaSpace read { person: Person =><br>  person.name == "john"<br> } | `=` {{% wbr %}} gigaSpace read new SQLQuery(classOf[Person], {{% wbr %}}  "name = ?", "john"{{% wbr %}}) |
|`!=` <br> predicateGigaSpace read { person: Person =><br>  person.name != "john"<br> } | `<>` {{% wbr %}} gigaSpace read new SQLQuery(classOf[Person], <br> "name <> ?", "john"<br>) |
|`>`  <br> predicateGigaSpace read { person: Person =><br>  person.height > 10<br>}| `>` {{% wbr %}}gigaSpace read new SQLQuery(classOf[Person], <br> "height > ?", 10: Integer<br>)|
|`>=` <br> predicateGigaSpace read { person: Person =><br>  person.height >= 10<br>} | `>=` {{% wbr %}} gigaSpace read new SQLQuery(classOf[Person], <br>  "height >= ?", 10: Integer<br>) |
|`<`  <br> predicateGigaSpace read { person: Person =><br> person.height < 10<br>}| `<` {{% wbr %}}  gigaSpace read new SQLQuery(classOf[Person], <br> "height < ?", 10: Integer<br>)|
|`<=` <br> predicateGigaSpace read { person: Person =><br>  person.height <= 10<br> } | `<=`{{% wbr %}}  gigaSpace read new SQLQuery(classOf[Person], <br>  "height <= ?", 10: Integer<br>) |
|`&&` <br> predicateGigaSpace read { person: Person =><br>  person.height > 10 && person.height < 100<br>} | `AND`{{% wbr %}} gigaSpace read new SQLQuery(classOf[Person], <br>  "( height > ? ) AND ( height < ? )", <br>  10: Integer, 100: Integer{{% wbr %}})|
|`||` <br> predicateGigaSpace read { person: Person =><br>  person.height < 10 \| person.height > 100<br>} | `OR`{{% wbr %}} gigaSpace read new SQLQuery(classOf[Person], <br> "( height < ? ) OR ( height > ? )", <br>  10: Integer, 100: Integer{{% wbr %}}) |
|`eq null` <br> predicateGigaSpace read { person: Person =><br>  person.name eq null<br> } | `is null`{{% wbr %}} gigaSpace read new SQLQuery(classOf[Person], <br> "name is null", QueryResultType.OBJECT<br> ) |
|`ne null` <br> predicateGigaSpace read { person: Person =><br>  person.name ne null<br> } | `is NOT null`{{% wbr %}} gigaSpace read new SQLQuery(classOf[Person], {{% wbr %}} "name is NOT null", QueryResultType.OBJECT<br>) |
|`like` <br>//  Implicit conversion on java.lang.String<br>predicateGigaSpace read { person: Person =><br>  person.name like "j%"<br>}| `like`{{% wbr %}} gigaSpace read new SQLQuery(classOf[Person], <br>  "name like 'j%'", QueryResultType.OBJECT{{% wbr %}}) |
|`notLike` <br>predicateGigaSpace read { person: Person =><br>  person.name notLike "j%"<br>} | `NOT like`{{% wbr %}} gigaSpace read new SQLQuery(classOf[Person], <br> "name NOT like 'j%'", QueryResultType.OBJECT{{% wbr %}}) |
|`rlike` <br>predicateGigaSpace read { person: Person =><br>  person.name rlike "j.\*"<br>} | `rlike`{{% wbr %}} gigaSpace read new SQLQuery(classOf[Person], <br> "name rlike 'j.\*'", QueryResultType.OBJECT<br>) |
|`Nested Queries` <br> predicateGigaSpace read { person: Person =><br> person.son.name == "dave"<br>} |{{% wbr %}}gigaSpace read new SQLQuery(classOf[Person], <br> "son.name = ?", "dave"{{% wbr %}}) |
|`Date` <br>// implicit conversion on java.util.Date<br>predicateGigaSpace read { person: Person =><br>  person.birthday < janesBirthday<br>} |{{% wbr %}}gigaSpace read new SQLQuery(classOf[Person], <br>  "birthday < ?", janesBirthday{{% wbr %}}) |
|`Date` <br> predicateGigaSpace read { person: Person =><br> person.birthday <= janesBirthday<br>} |{{% wbr %}}gigaSpace read new SQLQuery(classOf[Person], <br> "birthday <= ?", janesBirthday<br>) |
|`Date` <br> predicateGigaSpace read { person: Person =><br>  person.birthday > janesBirthday<br>} |{{% wbr %}}gigaSpace read new SQLQuery(classOf[Person], <br> "birthday > ?", janesBirthday<br>) |
|`Date` <br> predicateGigaSpace read { person: Person =><br>  person.birthday >= janesBirthday<br>} |{{% wbr %}}gigaSpace read new SQLQuery(classOf[Person], <br> "birthday >= ?", janesBirthday<br>) |
|`select` <br>// select is imported into scope<br>predicateGigaSpace read { person: Person =><br> select(person.name, person.birthday)<br> person.id == someId{{% wbr %}}} | {{% wbr %}}setProjections gigaSpace read new SQLQuery(classOf[Person], <br> "id = ?", someId<br>).setProjections("name, birthday") |
|`orderBy`<br>// orderBy is imported into scope<br>predicateGigaSpace read { person: Person =><br> orderBy(person.birthday)<br>  person.nickName eq null<br>} | `ORDER BY`{{% wbr %}} gigaSpace read new SQLQuery(classOf[Person], <br>  "nickName is null ORDER BY birthday", <br>  QueryResultType.OBJECT{{% wbr %}}) |
|`orderBy().ascending`<br>predicateGigaSpace read { person: Person =><br>  orderBy(person.birthday)==.ascending<br> person.nickName eq null<br>} | `ORDER BY ... ASC`{{% wbr %}} gigaSpace read new SQLQuery(classOf[Person], <br> "nickName is null ORDER BY birthday ASC", <br>  QueryResultType.OBJECT<br>) |
|`orderBy().descending`<br>predicateGigaSpace read { person: Person =><br>  orderBy(person.birthday).descending<br> person.nickName eq null<br>} | `ORDER BY ... DESC`{{% wbr %}} gigaSpace read new SQLQuery(classOf[Person], <br>  "nickName is null ORDER BY birthday DESC", <br>  QueryResultType.OBJECT<br>) |
|`groupBy`<br>// groupBy is imported into scope<br>predicateGigaSpace read { person: Person =><br>  groupBy(person.birthday)<br>  person.nickName eq null<br>} | `GROUP BY`{{% wbr %}} gigaSpace read new SQLQuery(classOf[Person], <br>  "nickName is null GROUP BY birthday", <br>  QueryResultType.OBJECT<br>) |
