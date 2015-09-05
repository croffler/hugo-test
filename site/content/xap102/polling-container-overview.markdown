---
layout: post102
title:  Polling Container
categories: XAP102
parent: event-processing.html
weight: 300
---

<br>


{{% imageltext "/attachment_files/subject/point-to-point.png" %}}
The polling event container is an implementation of the polling consumer pattern which uses the Space to receive events.
A polling event operation is mainly used when simulating Queue semantics or when using the master-worker design pattern.
{{% /imageltext %}}



<br>


{{%fpanel%}}

[Overview](./polling-container.html)<br>
The polling event container.

[Concurrent consumers](./polling-container-scaling.html)<br>
By default, the polling event container starts a single thread that performs the receive operations, and invokes the event listener. It can be configured to start several concurrent consumer threads.

[Transaction support](./polling-container-transactions.html)<br>
Both the receive operation and the actual event action can be configured to be performed under a transaction.

{{%/fpanel%}}

<br>

#### Additional Resources

{{<youtube "GwLfDYgl6f8" "Event Processing">}}


