---
layout: page
title: About CRDTs
permalink: /
---

<img src="{{ site.baseurl }}/assets/img/crdt-logo.png" style="width: 100%; max-width: 700px">

# About CRDTs

A **Conflict-free Replicated Data Type** (CRDT) is a data structure that
simplifies distributed data storage systems and multi-user applications.

In many systems, copies of some data need to be stored on multiple computers
(known as **replicas**). Examples of such systems include:

* Mobile apps that store data on the local device, and that need to sync that
  data to other devices belonging to the same user (such as calendars, notes,
  contacts, or reminders);
* Distributed databases, which maintain multiple replicas of the data (in the
  same datacenter or in different locations) so that the system continues
  working correctly if some of the replicas are offline;
* Collaboration software, such as Google Docs, Trello, Figma, or many others, in
  which several users can concurrently make changes to the same file or data;
* Large-scale data storage and processing systems, which replicate data in order
  to achieve global scalability.

All such systems need to deal with the fact that the data may be concurrently
modified on different replicas. Broadly speaking, there are two possible ways of
dealing with such data modifications:

Strongly consistent replication:
: In this model, the replicas coordinate with each other to decide when and how
  to apply the modifications. This approach enables strong consistency models
  such as serializable transactions and linearizability. However, waiting for
  this coordination reduces the performance of these systems; moreover, the CAP
  theorem tells us that it is impossible to make any data changes on a replica
  while it is disconnected from the rest of the system (e.g. due to a network
  partition, or because it is a mobile device with intermittent connectivity).

Optimistic replication:
: In this model, users may modify the data on any replica independently of any
  other replica, even if the replica is offline or disconnected from the others.
  This approach enables maximum performance and availability, but it can lead to
  conflicts when multiple clients or users concurrently modify the same piece of
  data. These conflicts then need to be resolved when the replicas communicate
  with each other.

Conflict-free Replicated Data Types (CRDTs) are used in systems with optimistic
replication, where they take care of conflict resolution. CRDTs ensure that, no
matter what data modifications are made on different replicas, the data can
always be merged into a consistent state. This merge is performed automatically
by the CRDT, without requiring any special conflict resolution code or user
intervention.

For more details on CRDTs, you can read the article
"[Conflict-free Replicated Data Types](https://arxiv.org/pdf/1805.06358.pdf)"
by Nuno Preguiça, Carlos Baquero, and Marc Shapiro (2018), or the older
"[A comprehensive study of Convergent and Commutative Replicated Data Types](https://hal.inria.fr/inria-00555588/document)"
by Marc Shapiro, Nuno Preguiça, Carlos Baquero, and Marek Zawirski (2011).
