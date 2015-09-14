---
type: post101
title:  Embedded Space
categories: XAP101NET
weight:
parent:
---

{{% ssummary %}}{{%/ssummary%}}



# Custom Properties

FIXTABLE
|Argument   | Dictionary<String,String> |
|Default    | none|
|Description|  |

Example:


```csharp
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

FIXTABLE
|Argument   | SecurityContext |
|Default    | none|
|Description||

Example:


```csharp
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

FIXTABLE
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:


```csharp
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

FIXTABLE
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:


```csharp
public void createSpaceWithFilter()
{
  TODO

}
```

# Gateway

FIXTABLE
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:


```csharp
public void createSpaceWithGateway()
{
  TODO

}
```


# LookupGroups

FIXTABLE
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:


```csharp
public void createSpaceWithLookupGroups()
{
  TODO

}
```


# LookupLocators

FIXTABLE
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:


```csharp
public void createSpaceWithLookupLocators()
{
  TODO

}
```


# LookupTimeout

FIXTABLE
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:


```csharp
public void createSpaceWithLookupTimeout()
{
  TODO

}
```


# Mirrored

FIXTABLE
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:


```csharp
public void createSpaceWithMirrored()
{
  TODO
}
```


# Name

FIXTABLE
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:


```csharp
public void createSpaceWithName()
{
  TODO
}
```

# Secured

FIXTABLE
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:


```csharp
public void createSpaceSecured()
{
  TODO
}
```


# Versioned

FIXTABLE
|Argument   | [ClusterInfo](http://www.gigaspaces.com/docs/dotnetdocs{{%currentversion%}}/html/T_GigaSpaces_Core_ClusterInfo.htm) |
|Default    | none|
|Description||

Example:


```csharp
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



