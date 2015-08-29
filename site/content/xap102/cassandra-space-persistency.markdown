---
layout: post102
title:  Cassandra Persistency
categories: XAP102
parent: cassandra.html
weight: 100
---


<br>


XAP comes with built in implementations of [Space Data Source](./space-data-source-api.html) and [Space Synchronization Endpoint](./space-synchronization-endpoint-api.html) for Cassandra, called `CassandraSpaceDataSource` and `CassandraSpaceSynchronizationEndpoint`, respectively.


![CassMirrorNew.jpg](/attachment_files/CassMirrorNew.jpg)

<br>

{{% comment %}}
For information about the two see: [Cassandra Space Data Source](./cassandra-space-data-source.html) and [Cassandra Space Synchronization Endpoint](./cassandra-space-synchronization-endpoint.html).
{{% /comment %}}

For further details about the persistency APIs used see [Space Persistency](./space-persistency.html).


## Related Topics

- [Data Source](./cassandra-space-data-source.html)<br>
The Space Data Source API is used for reading data and meta data from the Cassandra.

- [Synchronization Endpoint](./cassandra-space-synchronization-endpoint.html)<br>
The space synchronization endpoint API is used for synchronizing data from the space to Cassandra data base.

- [Hector Library](./cassandra-hector-client.html)<br>
Hector client library.



