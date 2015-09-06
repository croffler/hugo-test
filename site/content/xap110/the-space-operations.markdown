---
layout: post102
title:  Operations
categories: XAP102
weight: 300
parent: the-gigaspace-interface-overview.html
---


{{% ssummary %}}{{%/ssummary%}}


XAP provides a simple space API using the [GigaSpace](http://www.gigaspaces.com/docs/JavaDoc{{% currentversion %}}/org/openspaces/core/GigaSpace.html) interface for interacting with the space.


The interface includes the following main operations:

{{%section%}}
{{%column width="50%" %}}
{{%panel title="Write objects into the Space:"%}}
[write](#write) one object into the space<br>
[writeMultiple](#writeMultiple) objects into the Space<br>
[asynchronous write](#asynchronousWrite) to the Space
{{%/panel%}}
{{%/column%}}
{{%column width="50%" %}}
{{%panel title="Change objects in Space:"%}}
[change](#change) one object in Space<br>
		  [changeMultiple](./change-api.html) objects in Space <br>
[asynchronous change](./change-api.html) of objects
{{%/panel%}}
{{%/column%}}
{{%/section%}}


{{%section%}}
{{%column width="50%" %}}
{{%panel title="Reading objects from the Space:"%}}
[readById](#read) from the Space<br>
[readByIds](#readMultiple) from the Space<br>
[read](#read) object by template from the Space<br>
[readMultiple](#readMultiple) objects from the Space <br>
[read asynchronous](#asynchronousRead) from the Space <br>
[read if exists](#readIfExists) <br>
[read if exists by id](#readIfExists)
{{%/panel%}}
{{%/column%}}
{{%column width="50%" %}}
{{%panel "title=Removing objects from the Space:"%}}
[take](#take) object by template from Space<br>
[takeById](#take) object by id from Space<br>
[takeByIds](#takeMultiple) objects by ids from Space<br>
[takeMultiple](#takeMultiple) objects from Space <br>
[take asynchronous](#asynchronousTake)<br>
[take if exists](#takeIfExists)<br>
[clear](#clear) objects in Space
{{%/panel%}}
{{%/column%}}
{{%/section%}}

{{%section%}}
{{%column width="50%" %}}
{{%panel title="Other operations:"%}}
[aggregation](#aggregators)  across the Space<br>
[count](#count) objects in Space<br>
[counters](#counters) increment and decrement
{{%/panel%}}
{{%column width="50%" %}}
{{%/column%}}
{{%/column%}}
{{%/section%}}



# Simpler API

The `GigaSpace` interface provides a simpler space API by utilizing Java 5 generics, and allowing sensible defaults. Here are some examples of the space operations as defined within `GigaSpace`:

```java
public interface GigaSpace {
    <T> LeaseContext<T> write(T entry) throws DataAccessException;
    // ....
    <T> T read(ISpaceQuery<T> query, Object id)throws DataAccessException;
    // ......
    <T> T take(T template) throws DataAccessException;
    <T> T take(T template, long timeout) throws DataAccessException;
    // ......
}
```

In the example above, the take operation can be performed without specifying a timeout. The default take timeout is `0` (no wait), and can be overridden when configuring the `GigaSpace` factory. In a similar manner, the read timeout and write lease can be specified.


INCLUDEME
