+++

Description = ""
title = "Accordion"
menu = "howto"
weight= "100"
+++

# Accordion

{{%accordion %}}

{{%accord title="accord0"%}}
{{%highlight java%}} 

private int age;
private String name;
 
{{%/highlight%}}
{{%/accord%}}

{{%accord title="accord1"%}}
 
 fdslfsdkfldkfdsf
 dsfsdf
 sdfsdfdsf

{{%/accord%}}


{{%accord title="accordion3" %}}
 
 fdslfsdkfldkfdsf
 dsfsdf
 sdfsdfdsf

{{%/accord%}}

{{%/accordion%}}


# Accordion 2
 
{{%accordion test1%}}

{{%accord title="accordion1"  %}}
{{%highlight java%}}

private int age;
private String name;

{{%/highlight%}}
{{%/accord%}}

{{%accord title="accordion2"  %}}

 fdslfsdkfldkfdsf
 dsfsdf
 sdfsdfdsf

{{%/accord%}}


{{%accord title="accordion3"  %}}

 fdslfsdkfldkfdsf
 dsfsdf
 sdfsdfdsf

{{%/accord%}}

{{%/accordion%}}


# Complexe Accordion
{{%accordion%}}
{{%accord title="**Example**"  %}}


The following deploys a processing unit jar file named `data-processor.jar` using the `sync_replicated` cluster schema with 2 instances (`total_members`).

```bash
gs> deploy -cluster schema=sync_replicated total_members=2 data-processor.jar
```

The following deploys a processing unit archive called `data-processor.jar` using deployment properties file called `pu.properties`.

```bash
gs> deploy -properties file://config/pu.properties data-processor.jar

```

The following deploys a processing unit archive called `data-processor.jar` direct injecting the properties.

```bash
gs> deploy -properties embed://DB_username=postgres;DB_password=pass mirror
```

Using the following pu configuration:
```xml
<bean id="dataSource" class="org.apache.commons.dbcp.BasicDataSource" destroy-method="close">
    <property name="driverClassName" value="org.postgresql.Driver"/>
    <property name="url" value="jdbc:postgresql:presence"/>
    <property name="username" value="${DB_username}"/>
    <property name="password" value="${DB_password}"/>
</bean>

```

The following deploys a processing unit archive called `data-processor.jar` using an SLA element read from an external `sla.xml` file.
```bash
gs> deploy -sla file://config/sla.xml data-processor.jar
```

The following example deploys a `partitioned-sync2backup` space cluster with the name `mySpace` for both the processing unit and the Space it contains.

```bash
deploy -cluster schema=partitioned-sync2backup total_members=2,1 -override-name mySpace -properties embed://dataGridName=mySpace myPUFolder
```



{{% tip %}}
Multiple deployment properties can be injected by having ; between each property - see below example:

```java
>gs deploy -cluster schema=partitioned-sync2backup total_members=10,1
-properties "embed://dataGridName=myIMDG;space-config.proxy.router.active-server-lookup-timeout=5000;space-config.engine.max_threads=256;mypropA=aaa;mypropB=bbb" -override-name myPU /tmp/myPu.jar
```
{{% /tip %}}



{{% warning %}}
Multiple deployment properties can be injected by having ; between each property - see below example:

```java
>gs deploy -cluster schema=partitioned-sync2backup total_members=10,1
-properties "embed://dataGridName=myIMDG;space-config.proxy.router.active-server-lookup-timeout=5000;space-config.engine.max_threads=256;mypropA=aaa;mypropB=bbb" -override-name myPU /tmp/myPu.jar
```
{{% /warning %}}

{{%/accord%}}
{{%/accordion%}}


# Accordion with Table

{{%accordion %}}

{{%accord title="accord0"%}}

Keyname       | Required | Type          | Description
-----------   | -------- | ----          | -----------
type          | yes      | string        | The [node type](dsl-spec-node-types.html) of this node template.
properties    | no       | dict          | The properties of the node template matching its node type properties schema.
instances     | no       | dict          | Instances configuration.
interfaces    | no       | interfaces    | Used for mapping plugins to [interfaces](dsl-spec-interfaces.html) operation or for specifying inputs for already mapped node type operations.
relationships | no       | relationships | Used for specifying the [relationships](dsl-spec-relationships.html) this node template has with other node templates.

{{%/accord%}}

{{%/accordion%}}



# Accordion with Tabs

{{%accordion%}}
{{%accord title="Tabs in an accordion"%}}
{{%tabs%}}
{{%tab table%}}

Keyname       | Required | Type          | Description
-----------   | -------- | ----          | -----------
type          | yes      | string        | The [node type](dsl-spec-node-types.html) of this node template.
properties    | no       | dict          | The properties of the node template matching its node type properties schema.
instances     | no       | dict          | Instances configuration.
interfaces    | no       | interfaces    | Used for mapping plugins to [interfaces](dsl-spec-interfaces.html) operation or for specifying inputs for already mapped node type operations.
relationships | no       | relationships | Used for specifying the [relationships](dsl-spec-relationships.html) this node template has with other node templates.
{{%/tab%}}
{{%/tabs"}}

{{%/accord%}}
{{%/accordion%}}


<!--div class="row">
    <div class="easyui-accordion" style="width:500px;height:300px;">
            <div title="About" data-options="iconCls:'icon-ok'" style="overflow:auto;padding:10px;">
            <h3 style="color:#0099FF;">Accordion for jQuery</h3>
                <p>Accordion is a part of easyui framework for jQuery. It lets you define your accordion component on web page more easily.</p>
            </div>
            <div title="Help" data-options="iconCls:'icon-help'" style="padding:10px;">

             <div class="easyui-tabs"  >
                     <div title="About" style="padding:10px">
                         <p style="font-size:14px">jQuery EasyUI framework helps you build your web pages easily.</p>
                         <ul>
                             <li>easyui is a collection of user-interface plugin based on jQuery.</li>
                             <li>easyui provides essential functionality for building modem, interactive, javascript applications.</li>
                             <li>using easyui you don't need to write many javascript code, you usually defines user-interface by writing some HTML markup.</li>
                             <li>complete framework for HTML5 web page.</li>
                             <li>easyui save your time and scales while developing your products.</li>
                             <li>easyui is very easy but powerful.</li>
                         </ul>
                     </div>
                     <div title="My Documents" style="padding:10px">
                         <ul class="easyui-tree" data-options="url:'tree_data1.json',method:'get',animate:true"></ul>
                     </div>
                     <div title="Help" data-options="iconCls:'icon-help',closable:true" style="padding:10px">
                         This is the help content.
                     </div>
                 </div>
            </div>
            <div title="TreeMenu" data-options="iconCls:'icon-search'" style="padding:10px;">
                <ul class="easyui-tree">
                  <li>
                    <span>Foods</span>
                    <ul>
                        <li>
                            <span>Fruits</span>
                            <ul>
                                <li>apple</li>
                                <li>orange</li>
                            </ul>
                        </li>
                        <li>
                            <span>Vegetables</span>
                            <ul>
                                <li>tomato</li>
                                <li>carrot</li>
                                <li>cabbage</li>
                                <li>potato</li>
                                <li>lettuce</li>
                            </ul>
                        </li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>
</div-->

 