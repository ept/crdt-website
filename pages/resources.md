---
layout: page
title: CRDT Resources
permalink: /resources
---

# CRDT Resources

## Introductions to CRDTs

* Nuno Pregui&ccedil;a:
  [Conflict-free Replicated Data Types: An Overview](https://arxiv.org/abs/1806.10254).
  arXiv:1806.10254, June 2018.

* Marc Shapiro, Nuno Pregui&ccedil;a, Carlos Baquero, and Marek Zawirski:
  [A comprehensive study of Convergent and Commutative Replicated Data Types](http://hal.inria.fr/inria-00555588/).
  INRIA Research Report 7506, Jan. 2011.

* The [Wikipedia article on CRDTs](https://en.wikipedia.org/wiki/Conflict-free_replicated_data_type).

* [Awesome CRDT](https://github.com/alangibson/awesome-crdt): another collection of CRDT resources

* [Nikita Voloboev: "Everything I know"](https://wiki.nikitavoloboev.xyz/distributed-systems/crdt)

## Blog posts

* [Bartosz Sypytkowski](https://bartoszsypytkowski.com/): 12-part blog series on CRDTs. Parts
  [1](https://bartoszsypytkowski.com/the-state-of-a-state-based-crdts/),
  [2](https://bartoszsypytkowski.com/optimizing-state-based-crdts-1/),
  [3](https://bartoszsypytkowski.com/optimizing-state-based-crdts-part-2/),
  [4](https://bartoszsypytkowski.com/state-based-crdts-bounded-counter/),
  [5](https://bartoszsypytkowski.com/crdt-map/),
  [6](https://bartoszsypytkowski.com/operation-based-crdts-protocol/),
  [7](https://bartoszsypytkowski.com/operation-based-crdts-registers-and-sets/),
  [8](https://bartoszsypytkowski.com/operation-based-crdts-arrays-1/),
  [9](https://bartoszsypytkowski.com/operation-based-crdts-arrays-2/),
  [10](https://bartoszsypytkowski.com/operation-based-crdts-json-document/),
  [11](https://bartoszsypytkowski.com/pure-operation-based-crdts/),
  [12](https://bartoszsypytkowski.com/crdt-optimizations/)
  (2017–2021)

* Joseph Gentle (who worked on Google Wave):
  [I was wrong. CRDTs are the future](https://josephg.com/blog/crdts-are-the-future/)
  (September 2020)

* Kevin Jahns:
  [Are CRDTs suitable for shared editing?](https://blog.kevinjahns.de/are-crdts-suitable-for-shared-editing/)
  (August 2020)

* Lars Hupel:
  [An introduction to Conflict-free Replicated Data Types](https://lars.hupel.info/topics/crdt/01-intro)

  A blog post series focussed on the mathematical foundations of CRDTs, with interactive code examples (July 2020)

* Robert Lord:
  [Notes on Splicing CRDTs for Structured Hypertext](https://lord.io/blog/2019/splicing-crdts/)
  (October 2019)

* Christopher Meiklejohn:
  [Applied Monotonicity: A Brief History of CRDTs in Riak](http://christophermeiklejohn.com/erlang/lasp/2019/03/08/monotonicity.html)
  (March 2019)

* Jo Stichbury/Paddy Byers (Ably) [How do CRDTs solve distributed data consistency challenges?](https://ably.com/blog/crdts-distributed-data-consistency-challenges)

* Anton Zagorskii:
  [CRDT: Conflict-free Replicated Data Types](https://medium.com/@amberovsky/crdt-conflict-free-replicated-data-types-b4bfc8459d26)
  (August 2018)

* Alexei Baboulevitch (Archagon):
  [Data Laced with History: Causal Trees & Operational CRDTs](http://archagon.net/blog/2018/03/24/data-laced-with-history/)
  
  A detailed exposition of Causal Trees and its implementation. (March 2018)

  [Interactive Code Examples in Swift](https://github.com/archagon/crdt-playground)
  
* Rudi Chen:
  [A simple approach to building a real-time collaborative text editor](http://digitalfreepen.com/2017/10/06/simple-real-time-collaborative-text-editor.html)
  (October 2017)

* Russell Sullivan:
  [Datanet: A New CRDT Database That Let's You Do Bad Bad Things To Distributed Data](http://highscalability.com/blog/2016/10/17/datanet-a-new-crdt-database-that-lets-you-do-bad-bad-things.html)
  (October 2016)

* [John Mumm](http://jtfmumm.com/) has written a two-part introduction to CRDTs:
  [Part I: Defanging Order Theory](http://jtfmumm.com/blog/2015/11/17/crdt-primer-1-defanging-order-theory/) and
  [Part II: Convergent CRDTs](http://jtfmumm.com/blog/2015/11/24/crdt-primer-2-convergent-crdts/)
  (November 2015).
  
* [Matthew Weidner](https://mattweidner.com/):
  [Designing Data Structures for Collaborative Apps](https://mattweidner.com/2022/02/10/collaborative-data-design.html)
  (February 2022)

* Geoffrey Litt, Slim Lim, Martin Kleppmann, Peter van Hardenberg:
  [Peritext: A CRDT for Rich-Text Collaboration](https://www.inkandswitch.com/peritext/)
  (November 2021)

## Conference talk recordings

* Martin Kleppmann:
  [CRDTs: The Hard Parts](https://www.youtube.com/watch?v=x7drE24geUw)
  (Hydra distributed computing conference, July 2020)

* James Long:
  [CRDTs for Mortals](https://www.dotconferences.com/2019/12/james-long-crdts-for-mortals)
  (dotJS, December 2019)

* Martin Kleppmann:
  [Automerge: Making Servers Optional for Real-Time Collaboration](https://www.youtube.com/watch?v=GXJ0D2tfZCM)
  (TNG Big Techday, June 2019)
  ([slides](https://speakerdeck.com/ept/automerge-making-servers-optional-for-real-time-collaboration))
  
* Sun-Li Beatteay:
  [Guaranteeing Consensus in Distributed Systems with CRDTs](https://www.youtube.com/watch?v=1Bs3Fj9rvks)
  (Papers We Love NYC, April 2019)
  ([slides](https://www.slideshare.net/SunLiBeatteay/guaranteeing-consensus-in-distriubuted-systems-with-crdts))

* Антон Чапоргин (Anton Chaporgin):
  [Редактор текста на CRDT в продакшене](https://2019.codefest.ru/lecture/1501)
  (CRDT text editor in production), Code Fest, March 2019
  ([slides](https://speakerdeck.com/codefest/codefest-2019-anton-chaporghin-iandieks-riedaktor-tieksta-na-crdt-v-prodakshienie))

* Pedro Teixeira:
  [CRDTs in IPFS](https://www.youtube.com/watch?v=2VOF-Z-nLnQ)
  (IPFS Lisbon Meetup, January 2018)

* Carlos Baquero:
  [CRDTs and Redis&mdash;From Sequential to Concurrent Executions](https://www.youtube.com/watch?v=ZoMIzBM0nf4)
  (RedisConf 2018)

* Martin Kleppmann:
  [Convergence versus Consensus: CRDTs and the Quest for Distributed Consistency](https://www.infoq.com/presentations/crdt-distributed-consistency/)
  (QCon London, March 2018)
  ([slides](https://speakerdeck.com/ept/convergence-versus-consensus-crdts-and-the-quest-for-distributed-consistency))

* Annette Bieniusa:
  [Antidote - a Scalable and Consistent Transactional Data Store](http://www.erlang-factory.com/euc2016/annette-bieniusa)
  (Erlang User Conference 2016)

* Dmitry Ivanov & Nami Naserazad:
  [Practical Demystification of CRDT](https://www.youtube.com/watch?v=PQzNW8uQ_Y4)
  (Lambda Days 2016)

* Martin Kleppmann:
  [Conflict Resolution for Eventual Consistency](https://www.youtube.com/watch?v=yCcWpzY8dIA)
  (GOTO Berlin 2016)

* Arnout Engelen:
  [CRDTs Illustrated](https://www.youtube.com/watch?v=9xFfOhasiOE)
  (Strange Loop 2015)

* Marc Shapiro & Nuno Pregui&ccedil;a:
  [CRDTs in Practice](https://www.youtube.com/watch?v=xxjHC3yLDqw)
  (Code Mesh 2015)

* Alexander Songe:
  [CRDT: Datatype for the Apocalypse](https://www.youtube.com/watch?v=txD1tfyIIvY)
  (ElixirConf 2015)

* Peter Bourgon:
  [Consistency without consensus in production systems](https://www.youtube.com/watch?v=em9zLzM8O7c)
  (Strange Loop 2014)

* Various:
  [PaPoC 2020 Recorded Talks](https://www.youtube.com/playlist?list=PLHHiNr_VnyWKj64PWjd9iM2OY19s9QGCY)
  (PaPoC 2020)
