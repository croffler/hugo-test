---
layout: post102
title:  Operations
categories: XAP102
weight: 300
parent: the-gigaspace-interface-overview.html
---


{{% summary %}}{{%/summary%}}


XAP provides a simple space API using the [GigaSpace](http://www.gigaspaces.com/docs/JavaDoc{{% currentversion %}}/org/openspaces/core/GigaSpace.html) interface for interacting with the space.


The interface includes the following main operations:

{{%section%}}
{{%column width=50% %}}
{{%panel bgColor=white | title=Write objects into the Space:%}}
[write](#write) one object into the space<br>
[writeMultiple](#writeMultiple) objects into the Space<br>
[asynchronous write](#asynchronousWrite) to the Space
{{%endpanel%}}
{{%/column%}}
{{%column width=50% %}}
{{%panel bgColor=white | title=Change objects in Space:%}}
[change](#change) one object in Space<br>
		  [changeMultiple](./change-api.html) objects in Space <br>
[asynchronous change](./change-api.html) of objects
{{%endpanel%}}
{{%/column%}}
{{%/section%}}


{{%section%}}
{{%column width=50% %}}
{{%panel bgColor=white |  title=Reading objects from the Space:%}}
[readById](#read) from the Space<br>
[readByIds](#readMultiple) from the Space<br>
[read](#read) object by template from the Space<br>
[readMultiple](#readMultiple) objects from the Space <br>
[read asynchronous](#asynchronousRead) from the Space <br>
[read if exists](#readIfExists) <br>
[read if exists by id](#readIfExists)
{{%endpanel%}}
{{%/column%}}
{{%column width=50% %}}
{{%panel bgColor=white |  title=Removing objects from the Space:%}}
[take](#take) object by template from Space<br>
[takeById](#take) object by id from Space<br>
[takeByIds](#takeMultiple) objects by ids from Space<br>
[takeMultiple](#takeMultiple) objects from Space <br>
[take asynchronous](#asynchronousTake)<br>
[take if exists](#takeIfExists)<br>
[clear](#clear) objects in Space
{{%endpanel%}}
{{%/column%}}
{{%/section%}}

{{%section%}}
{{%column width=50% %}}
{{%panel bgColor=white |  title=Other operations:%}}
[aggregation](#aggregators)  across the Space<br>
[count](#count) objects in Space<br>
[counters](#counters) increment and decrement
{{%endpanel%}}
{{%column width=50% %}}
{{%/column%}}
{{%/column%}}
{{%/section%}}

{{%comment%}}

{: .table .table-bordered}
|[Id Based operations](./id-queries.html)|[Batch operations](#Batch Operations)|[Asynchronous operations](#Asynchronous Operations)|Data Count operations|
|:--|:--|:--|:--|
|[readById](./id-queries.html#Reading an Object using its ID){{% wbr %}}takeById{{% wbr %}}[readByIds](./id-queries.html#Reading Multiple Objects using their IDs){{% wbr %}}takeByIds{{% wbr %}}readIfExistsById{{% wbr %}}takeIfExistsById|readMultiple{{% wbr %}}takeMultiple{{% wbr %}}[writeMultiple](#writeMultiple){{% wbr %}}readByIds{{% wbr %}}takeByIds|asyncRead{{% wbr %}}asyncTake{{% wbr %}}asyncChange{{% wbr %}}execute|count|

{: .table .table-bordered}
|[Data Query operations](./query-sql.html)|Data Insert and Update operations|[Business logic execution operations](./task-execution-over-the-space.html)|Data removal operations|
|:--|:--|:--|:--|
|read{{% wbr %}}readMultiple{{% wbr %}}[iterator](./query-paging-support.html)|write{{% wbr %}}writeMultiple{{% wbr %}}   [change](./change-api.html) |execute{{% wbr %}}executorBuilder|clean{{% wbr %}}clear{{% wbr %}}take{{% wbr %}}takeMultiple|

{{%/comment%}}

# Simpler API

The `GigaSpace` interface provides a simpler space API by utilizing Java 5 generics, and allowing sensible defaults. Here are some examples of the space operations as defined within `GigaSpace`:

{{% highlight java %}}
public interface GigaSpace {
    <T> LeaseContext<T> write(T entry) throws DataAccessException;
    // ....
    <T> T read(ISpaceQuery<T> query, Object id)throws DataAccessException;
    // ......
    <T> T take(T template) throws DataAccessException;
    <T> T take(T template, long timeout) throws DataAccessException;
    // ......
}
{{% /highlight %}}

In the example above, the take operation can be performed without specifying a timeout. The default take timeout is `0` (no wait), and can be overridden when configuring the `GigaSpace` factory. In a similar manner, the read timeout and write lease can be specified.




{{% include /COM/xap102/ops-write.markdown %}}
{{% include /COM/xap102/ops-change.markdown %}}
{{% include /COM/xap102/ops-read.markdown %}}
{{% include /COM/xap102/ops-take.markdown %}}
{{% include /COM/xap102/ops-clear.markdown %}}
{{% include /COM/xap102/ops-count.markdown %}}
{{% include /COM/xap102/ops-counters.markdown %}}
{{% include /COM/xap102/ops-aggregation.markdown %}}
{{% include /COM/xap102/ops-async-extension.markdown %}}
