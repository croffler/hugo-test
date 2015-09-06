---
layout: post102
title:  Metadata Summary
categories:
parent: space-based-remoting-overview.html
weight: 400
---

{{% ssummary %}}{{% /ssummary %}}


# RemotingService


|Class Annotation    | @RemotingService|
|Description         | Spring provides support for various remoting technologies. GigaSpaces uses the same concepts to provide remoting, using the space as the underlying protocol |
|Attribute Annotation| @ExecutorProxy  |
|Method argument     | @Routing |


{{% accordion acc1 %}}
{{%accord tithe="**Example**" parent="acc1" id="tab1"%}}
```java
// Service Implementation
@RemotingService
public class DataProcessor implements IDataProcessor {

    public Data processData(Data data) {
    	data.setProcessor(true);
    	return data;
    }
}

// Client remoting proxy
public class DataRemoting {

    @ExecutorProxy
    private IDataProcessor dataProcessor;

    // ...
}

// remote method with routing parameter
public interface MyService {

    void doSomething(@Routing int param1, int param2);
}
```
{{% /accord %}}
{{% /accordion %}}

{{%learn "./space-based-remoting.html"%}}


# ExecutorProxy


|Attribute Annotation| @ExecutorProxy  |
|Description         | Spring provides support for various remoting technologies. GigaSpaces uses the same concepts to provide remoting, using the space as the underlying protocol |


{{% accordion acc2 %}}
{{%accord tithe="**Example**" parent="acc2" id="tab2"%}}

```java
// Client remoting proxy
public class DataRemoting {

    @ExecutorProxy
    private IDataProcessor dataProcessor;

    // ...
}
```
{{% /accord %}}
{{% /accordion %}}

{{%learn "./space-based-remoting.html"%}}


# Routing


|Method argument     | @Routing |
|Description         | Spring provides support for various remoting technologies. GigaSpaces uses the same concepts to provide remoting, using the space as the underlying protocol |



{{% accordion acc3 %}}
{{%accord title="**Example**" %}}
```java
// Service Implementation
@RemotingService

   // remote method with routing parameter
   public interface MyService {

    void doSomething(@Routing int param1, int param2);
}
```
{{% /accord %}}
{{% /accordion %}}

{{%learn "./space-based-remoting.html"%}}