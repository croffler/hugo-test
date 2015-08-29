---
layout: post102
title: Mongo Persistency
categories: XAP102
parent: mongodb.html
weight: 100
---


{{%comment%}}
{{% ssummary %}} A MongoDB Space Persistency Solution {{% /ssummary %}}
{{%/comment%}}


XAP comes with built in implementations of [Space Data Source](./space-data-source-api.html) and [Space Synchronization Endpoint](./space-synchronization-endpoint-api.html)
 for MongoDB, called `MongoSpaceDataSource` and `MongoSpaceSynchronizationEndpoint`, respectively.

<br>

![mongodbPersistence.jpg](/attachment_files/mongodbPersistence.jpg)


{{% comment %}}
For information about the two see: [MongoDB Space Data Source](./mongodb-space-data-source.html) and [MongoDB Space Synchronization Endpoint](./mongodb-space-synchronization-endpoint.html).
{{% /comment %}}

For further details about the persistency APIs used see [Space Persistency](./space-persistency.html).


## Related Topics

- [Data Source](./mongodb-space-data-source.html)<br>
The Space Data Source API is used for reading data and meta data from the MongoDB.

- [Synchronization Endpoint](./mongodb-space-synchronization-endpoint.html)<br>
The space synchronization endpoint API is used for synchronizing data from the space to MongoDB data base.
