---
layout: post102
title:  Embedded Space
categories: XAP102NET
weight:
parent:
---

{{% ssummary %}}{{%/ssummary%}}



# Custom Properties

{: .table   .table-condensed  .table-bordered}
|Argument   | Dictionary<String,String> |
|Default    | none|
|Description|  |

Example:

```c#
public void createSpaceWithProperties()
{
    Dictionary<String,String> properties = new Dictionary<String,String> ();
	properties.Add ("fifo", "true");
	properties.Add ("lookupGroups", "test");

    // Create the factory
	EmbeddedSpaceFactory factory = new EmbeddedSpaceFactory ("mySpace");

	// Set the properties
	factory.CustomProperties = properties;

	//create the ISpaceProxy
	ISpaceProxy proxy = factory.Create ();

	// .......
	proxy.Dispose ();
}
```

# Security

{: .table   .table-condensed  .table-bordered}
|Argument   | SecurityContext |
|Default    | none|
|Description||

Example:

```c#
public void createSpaceWithCredentials()
{
    SecurityContext securityContext = new SecurityContext ("userName", "password");

	// Create the factory
	EmbeddedSpaceFactory factory = new EmbeddedSpaceFactory ("mySpace");

    // Set the Security Context
	factory.Credentials = securityContext;

	//create the ISpaceProxy
	ISpaceProxy proxy = factory.Create ();

	// .......
	proxy.Dispose ();
}
```

# Cluster Info

{: .table   .table-condensed  .table-bordered}
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:

```c#
public void createSpaceWithClusterInfo()
{
    // Cluster info settings
	ClusterInfo clusterInfo = new ClusterInfo ();
	clusterInfo.NumberOfBackups = 1;
	clusterInfo.Schema = "sync_replication";
	// Create the factory
	EmbeddedSpaceFactory factory = new EmbeddedSpaceFactory ("mySpace");
	// Set the Cluster Info
	factory.ClusterInfo = clusterInfo;
	//create the ISpaceProxy
	ISpaceProxy proxy = factory.Create ();
	// .......
	proxy.Dispose ();
}
```

### ClusterInfo





# Filters

{: .table   .table-condensed  .table-bordered}
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:

```c#
public void createSpaceWithFilter()
{
  TODO

}
```

# Gateway

{: .table   .table-condensed  .table-bordered}
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:

```c#
public void createSpaceWithGateway()
{
  TODO

}
```


# LookupGroups

{: .table   .table-condensed  .table-bordered}
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:

```c#
public void createSpaceWithLookupGroups()
{
  TODO

}
```


# LookupLocators

{: .table   .table-condensed  .table-bordered}
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:

```c#
public void createSpaceWithLookupLocators()
{
  TODO

}
```


# LookupTimeout

{: .table   .table-condensed  .table-bordered}
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:

```c#
public void createSpaceWithLookupTimeout()
{
  TODO

}
```


# Mirrored

{: .table   .table-condensed  .table-bordered}
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:

```c#
public void createSpaceWithMirrored()
{
  TODO
}
```


# Name

{: .table   .table-condensed  .table-bordered}
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:

```c#
public void createSpaceWithName()
{
  TODO
}
```

# Secured

{: .table   .table-condensed  .table-bordered}
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:

```c#
public void createSpaceSecured()
{
  TODO
}
```


# Versioned

{: .table   .table-condensed  .table-bordered}
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:

```c#
public void createSpaceVersioned()
{
  TODO
}
```



	//Filters
		//Clustered
		//Gateway
		//LookupGroups
		//LookupLocators
		//LookupTimeout
		//Mirrored
		//Name
		//Secured
		//SpaceTypes
		//Versioned



