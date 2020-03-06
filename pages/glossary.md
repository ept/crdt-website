---
layout: page
title: CRDT Glossary
permalink: /glossary
---

# CRDT Glossary

Commutative Replicated Data Type (CmRDT):
: An old name for "operation-based CRDT". The term "operation-based" is now preferred.

Concurrent:
: Two events are concurrent if they happened without knowledge of each other
  (i.e. the node on which event A occurred had not heard of event B at the time
  of A, and vice versa).

Convergence:
: The key correctness property of CRDTs. Convergence requires the following: for
  any two replicas, if they have processed the same set of updates, then those
  replicas must be in the same state (regardless of the order in which they
  processed those updates).

Convergent Replicated Data Type (CvRDT):
: An old name for "state-based CRDT". The term "state-based" is now preferred.

Delta-CRDT:
: A variant of a state-based CRDT in which replicas don't always send their
  entire state, but rather send state differences (deltas). See
  [Delta State Replicated Data Types](https://arxiv.org/abs/1603.01529) by
  Paulo Sérgio Almeida, Ali Shoker, and Carlos Baquero.

Effector:
: In operation-based CRDTs, an effector is a function that updates the state of
  a replica by applying an operation.

Generator:
: In operation-based CRDTs, a generator is a function that processes a data
  modification action taken by a user, and produces an operation that can be
  sent over the network and applied by an effector.

Last write wins (LWW):
: A timestamp is attached to each update, and updates with higher timestamps
  always overwrite values written by updates with lower timestamps. However, if
  a replica has already applied an update with a higher timestamp, and it
  subsequently receives an update with a lower timestamp, the latter update is
  ignored. This approach is one way of ensuring convergence.

Observed-remove set (ORSet):
: Another name for add-wins set. "Add-wins" is now preferred.

Operation-based CRDT:
: A CRDT in which each modification of the replicated data is encoded as an
  operation, and operations are sent over the network. The system must ensure
  that operations are not lost (by resending if necessary) and that each
  operation is applied once (by ignoring duplicates). Operation-based CRDTs
  ensure that any two concurrent operations commute; that is, replicas can apply
  those operations in either order, and the outcome is the same.

Optimistic replication:
: An approach to replication in which a replica can process updates locally,
  without waiting for communication with other replicas. This means that
  replicas can become temporarily inconsistent, but CRDTs ensure that replicas
  nevertheless converge towards a consistent state (see Strong Eventual
  Consistency). See [Optimistic Replication](https://core.ac.uk/download/pdf/22879037.pdf)
  by Yasushi Saito and Marc Shapiro.

Replication:
: maintaining a copy of some data on multiple computing devices (maybe servers,
  maybe end-user devices). Those copies are called *replicas*.

State-based CRDT:
: A CRDT in which replicas synchronise by sending each other their entire state
  over the network; when one replica receives such a state from another replica,
  it uses a merge function to combine the two states. This merge function is
  defined in such a way that it is commutative (i.e. `merge(a,b) = merge(b,a)`),
  associative (i.e. `merge(a,merge(b,c)) = merge(merge(a,b),c)`), and idempotent
  (i.e. `merge(a,a)=a`).

Strong Eventual Consistency (SEC):
: A formal consistency model for CRDTs. It requires convergence (see above) and
  eventual delivery (if one replica has processed an update, every other replica
  that has not failed will also eventually process it). See
  [Conflict-Free Replicated Data Types](https://pages.lip6.fr/Marek.Zawirski/papers/RR-7687.pdf)
  by Marc Shapiro, Nuno Preguiça, Carlos Baquero, and Marek Zawirski.

Tombstone:
: A special object used in some CRDTs to indicate that a value is absent (e.g.
  because it has been deleted). Tombstones may increase the memory consumption
  of a CRDT, as they continue to exist even if the corresponding data has been
  deleted at the application level. There are algorithms for garbage-collecting
  tombstones and freeing their memory.
