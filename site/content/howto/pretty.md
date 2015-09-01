+++

Description = ""
title = "Table"

+++





<p>
 <pre class="prettyprint lang-bash1">
 > show
 </pre>
</p>

# hello

<p>
<pre class="prettyprint lang-java">
// Read an entry of type MyClass whose num property is greater than 500:
MyClass result1 = gigaSpace.read(new SQLQuery<MyClass>(MyClass.class, "num > 500"));

// Take an entry of type MyClass whose num property is less than 500:
MyClass result2 = gigaSpace.take(new SQLQuery<MyClass>(MyClass.class, "num < 500"));

MyClass[] results;
// Read all entries of type MyClass whose num is between 1 and 100:
results = gigaSpace.readMultiple(new SQLQuery<MyClass>(MyClass.class, "num >= 1 AND num <= 100"));

// Read all entries of type MyClass who num is between 1 and 100 using BETWEEN syntax:
results = gigaSpace.readMultiple(new SQLQuery<MyClass>(MyClass.class, "num BETWEEN 1 AND 100"));

// Read all entries of type MyClass whose num is either 1, 2, or 3:
results = gigaSpace.readMultiple(new SQLQuery<MyClass>(MyClass.class, "num IN (1,2,3)"));

// Read all entries of type MyClass whose num is greater than 1,
// and order the results by the name property:
results = gigaSpace.readMultiple(new SQLQuery<MyClass>(MyClass.class, "num > 1 ORDER BY name"));
  </pre>
</p>

# XML





<pre class="prettyprint lang-xml">
<code class=""java">
<beans>
    <os-core:embedded-space id="space" name="mySpace">
        <os-core:properties>
            <props>
                <prop key="space-config.QueryProcessor.date_format">yyyy-MM-dd HH:mm:ss</prop>
                <prop key="space-config.QueryProcessor.time_format">HH:mm:ss</prop>
            </props>
        </os-core:properties>
    </os-core:embedded-space>
</beans>
</code?

  </pre>


