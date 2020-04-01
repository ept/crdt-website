---
layout: page
title: Code
permalink: /implementations
---

# Code (Implementations)

## General-purpose CRDT libraries

There are several open source CRDT libraries that can be used to build
collaborative applications and replicated storage systems:

* [Automerge](https://github.com/automerge/automerge)
  ([extended abstract](https://mobiuk.org/abstract/S4-P5-Kleppmann-Automerge.pdf))
  is a JavaScript CRDT implementation with a JSON data model. Network
  communication is handled by a separate layer, such as
  [Hypermerge](https://github.com/automerge/hypermerge) (which uses [Dat](https://docs.datproject.org/)) or
  [plain TCP connections](https://github.com/automerge/automerge-net).

* [GUN](https://gun.eco/) ([GitHub](https://github.com/amark/gun))
  is a graph CRDT implemented in JavaScript, using WebRTC networking.
  It includes public-key-based user authentication and encryption.
  
* [kappa-db](https://github.com/kappa-db/) is a JavaScript library for building your own CRDTs over append-only log architectures, with a reference implementation for [Dat](https://docs.datproject.org/)'s Hypercore data structure. Sort of a 'build-your-own' Automerge library.

* [Replicated Object Notation](http://replicated.cc/) (RON) is a data format for
  encoding CRDT operations, implemented in
  [several languages](http://replicated.cc/impl/).
  It supports register, list, text, set, and counter datatypes.
  [SwarmDB](https://github.com/gritzko/swarm) is a RON-based database, implemented in JavaScript.

* [Yjs](https://github.com/yjs/yjs)
  ([paper 1](http://dbis.rwth-aachen.de/~derntl/papers/preprints/icwe2015-preprint.pdf),
  [paper 2](https://www.researchgate.net/publication/310212186_Near_Real-Time_Peer-to-Peer_Shared_Editing_on_Extensible_Data_Types))
  is a modular framework for building collaborative applications on the web.
  It includes several common CRDTs and modules that integrate them with different editors,
  communication protocols, and databases. More information in
  [this series of blog posts about Yjs](https://tag1consulting.com/yjs).

* [Legion](https://legion.di.fct.unl.pt/)
  ([GitHub](https://github.com/albertlinde/Legion),
  [paper](https://novasys.di.fct.unl.pt/~alinde/publications/fp0964-vanderlinde.pdf))
  provides a JavaScript implementation of counter, set, map, and list CRDTs, and
  a WebRTC-based networking layer.

* [Yorkie](https://yorkie.dev/) ([GitHub](https://github.com/yorkie-team/yorkie))
  is a synchronization solution for building collaborative applications, using MongoDB
  for data storage.

* The [Akka actor framework](https://akka.io/) includes implementations of
  [several CRDTs](https://doc.akka.io/docs/akka/2.6.3/typed/distributed-data.html#replicated-data-types).

* [Schism](https://github.com/aredington/schism) is a Clojure implementation of
  several CRDTs.

* [Erlang implementation](https://github.com/lasp-lang/types) of CRDTs from the
  [Lasp system](https://lasp-lang.readme.io/)

* Carlos Baquero's [C++ implementation](https://github.com/CBaquero/delta-enabled-crdts)
  of state-based CRDTs with delta mutations.

* [Logux](https://logux.io/) ([GitHub](https://github.com/logux/core)) is a state sync system built primarily for React/Redux in a client/server architecture, but can be used p2p and/or on its own.

* [Braid-HTTP](https://braid.news/) ([GitHub](https://github.com/braid-work/toomim-braidjs/)) is an effort to augment the HTTP protocol itself to include state synchronization as a primitive. [IETF draft](https://datatracker.ietf.org/doc/html/draft-toomim-httpbis-braid-http).

## Benchmarks

* [crdt-benchmarks](https://github.com/dmonad/crdt-benchmarks) compares document size and performance of Yjs and Automerge.


## Distributed databases

Several distributed databases also have built-in support for CRDTs:

* [AntidoteDB](https://www.antidotedb.eu/) is a geo-replicated database that
  supports highly available transactions, causal consistency, and
  [several CRDTs](https://antidotedb.gitbook.io/documentation/architecture/datatypes).

* The [Riak database](https://riak.com/) was one of the first to add
  [CRDT support](https://docs.riak.com/riak/kv/latest/developing/data-types/index.html) in
  [2013](http://christophermeiklejohn.com/erlang/lasp/2019/03/08/monotonicity.html)
  ([implemented in Erlang](https://github.com/basho/riak_dt)).

* [Soundcloud's Roshi](https://github.com/soundcloud/roshi) implements a set
  CRDT layer on top of a Redis storage backend.

* [Microsoft Azure CosmosDB](https://azure.microsoft.com/en-us/services/cosmos-db/)
  allows conflicting values to be merged either
  [using CRDTs](https://azure.microsoft.com/en-us/blog/azure-cosmos-db-pushing-the-frontier-of-globally-distributed-databases/),
  or using custom merge procedures.

* [Redis Enterprise](https://redislabs.com/redis-enterprise/)
  (a commercial extension of Redis)
  [uses CRDTs](https://www.redislabs.com/redis-enterprise/technology/active-active-geo-distribution/)
  to enable multi-master replication between geographically distributed
  datacenters.

* [Ditto](https://www.ditto.live) uses CRDTs for data sync between mobile devices.

* [OrbitDB](https://github.com/orbitdb/orbit-db) is a peer-to-peer database
  built on top of [IPFS](https://ipfs.io/) and CRDTs.

* The [Dynomite](https://github.com/Netflix/dynomite) storage system from
  Netflix [uses CRDTs](https://qconsf.com/sf2019/presentation/modern-cs)
  internally.

* [Weaveworks Mesh](https://github.com/weaveworks/mesh) is a gossip-based
  replication system
  [based on CRDTs](https://www.infoq.com/presentations/weave-mesh/).

* Facebook's internal
  [Apollo database](https://dzone.com/articles/facebook-announces-apollo-qcon)
  supports CRDT storage.

* Macrometa
  [Global Data Network (GDN)](https://www.macrometa.co/)
  allows conflicting documents and graphs to be merged using operation-based CRDTs and stream-based geo-replication, while providing higher level SQL-like query language interface.

## Text editors

Several text editors use CRDTs:

* The [Teletype package](https://teletype.atom.io/) for the
  [Atom text editor](https://atom.io/) uses
  [a CRDT](https://github.com/atom/teletype-crdt) to enable real-time
  collaboration
  ([talk](https://www.infoq.com/presentations/crdt-tachyon-collaborative-editing/)).
  [Tandem](https://github.com/typeintandem/tandem) further extends this support
  to other text editors.

* The [Conclave text editor](https://conclave-team.github.io/conclave-site/)
  (a research project) supports peer-to-peer collaboration based on the
  [LSEQ CRDT](https://hal.archives-ouvertes.fr/hal-00921633/document).

* [MUTE](https://github.com/coast-team/mute) (the Multi-User Text Editor,
  a research project) also supports CRDT-based peer-to-peer collaboration.

* The [Xi text editor](http://abishov.com/xi-editor/) is currently only
  single-user, not collaborative, but it nevertheless
  [uses CRDTs internally](http://abishov.com/xi-editor/docs/crdt-details.html)
  to allow plugins to run concurrently with the user thread, and hence improve
  performance.

* Apple's [Notes app](https://support.apple.com/en-us/HT205773) on iOS appears to be
  [built upon CRDTs](https://github.com/dunhamsteve/notesutils/blob/master/notes.md),
  as evidenced by
  [header files](https://github.com/nst/iOS-Runtime-Headers/blob/master/PrivateFrameworks/NotesShared.framework/TTMergeableString.h)
  in the operating system.

* [PeerPad](https://peerpad.net/) ([GitHub](https://github.com/peer-base/peer-pad))
  is a collaborative text editor based on IPFS and CRDTs.


## Other applications

Several other applications and systems also use CRDTs internally:

* [Actual](https://actualbudget.com/), a budgeting app,
  [uses CRDTs](https://jlongster.com/using-crdts-in-the-wild) to allow sync
  across multiple user devices.

* [Figma](https://www.figma.com/), a collaborative graphic design app,
  [uses CRDTs](https://www.figma.com/blog/how-figmas-multiplayer-technology-works/)
  (and occasionally a central server to simplify things) as well.

* [Pixelboard](https://www.getpixelboardapp.com/), a collaborative whiteboarding app,
  [uses CRDTs](https://medium.com/bpxl-craft/building-a-peer-to-peer-whiteboarding-app-for-ipad-2a4c7728863e)
  to allow several people to draw at the same time.

* [TomTom](https://www.tomtom.com/) GPS navigation systems
  [use CRDTs](https://speakerdeck.com/ajantis/practical-data-synchronization-with-crdts-strangeloop-2016)
  to synchronise user data, such as favourite locations, across multiple devices.

* Facebook's [OpenR](https://github.com/facebook/openr) routing platform internally
  [uses CRDTs](https://github.com/facebook/openr/blob/master/openr/docs/KvStore.md)
  to manage its state.

* [Bet365](https://www.infoq.com/articles/key-lessons-learned-from-transition-to-nosql/),
  [League of Legends](http://highscalability.com/blog/2014/10/13/how-league-of-legends-scaled-chat-to-70-million-players-it-t.html), and
  [PayPal](https://www.infoq.com/presentations/crdt-production/)
  have all reported using CRDTs internally.

* [Mapeo](https://mapeo.world), a toolset mapping and monitoring human and environmental rights abuses [uses CRDTs](https://www.digital-democracy.org/blog/localfirst/) for syncronizing edits to maps. 

* [Cobox](https://cobox.cloud), a collaborative data hosting platform [uses CRDTs](https://develop.cobox.cloud/core_technologies.html#kappa-core) to syncronize edits to files on disk.


## Automerge users

Several collaborative (multi-user, multi-device) applications have been built
using the [Automerge](https://github.com/automerge/automerge) CRDT library:

* [PushPin](https://automerge.github.io/pushpin/) is a digital workspace for
  media and notes on a 2D canvas.

* [PixelPusher](https://github.com/automerge/pixelpusher#readme)
  ([blog post](https://medium.com/@pvh/pixelpusher-real-time-peer-to-peer-collaboration-with-react-7c7bc8ecbf74))
  is a multi-user pixel art editor.

* [Trellis](https://github.com/automerge/trellis#readme)
  ([demo video](https://www.youtube.com/watch?v=L9fdyDlhByM))
  is a project management tool modelled after [Trello](https://trello.com/).

* [Capstone](https://github.com/inkandswitch/capstone#readme)
  ([article](https://www.inkandswitch.com/capstone-manuscript.html))
  is a tablet app for taking notes and thinking through ideas.

* [Archbee](https://archbee.io/) is a documentation tool and knowledge base for
  engineering teams.

## Yjs users

[Yjs](https://github.com/yjs/yjs) is used by several apps that are run in production:

* [Room.sh](https://room.sh/) is a meeting application with integrated collaborative drawing, editing, and coding tools.

* [Pluxbox - Radiomanager](https://pluxbox.com/) is a web-based app to collaboratively organize radio broadcasts.

* [Cattaz](http://cattaz.io/) is a wiki that can run custom applications in the wiki pages.
