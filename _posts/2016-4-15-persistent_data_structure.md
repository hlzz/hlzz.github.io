---
layout: post
title: MIT 6.851 Lesson 1 - Making Data Structures Persistent (高级数据结构 L1 - 持久化数据结构)
---
I started watching [MIT 6.851](https://www.youtube.com/playlist?list=PLUl4u3cNGP61hsJNdULdudlRL493b-XZf) (Advanced Data Structures) by Professor Eric Demaine on YouTube a year ago, but often give it up halfway. So this time I decided to document my progress 
to keep me committed. I would watch some of the lecture videos before going to bed and then write down some notes next morning. Let's get started!

The first lecture concerns with persistent data structures. The topic is broad and I cannot grasp all the essence solely by watching the lectures. 
Therefore some reference reading is necessary to catch up with the course. The following content is based on the lecture and some reference materials.

## Four types of persistency [2]  

* Partially persistent: may query any previous version of the data structure, but we may only update the latest version.  

* Fully persistent: both updates and queries are allowed on any version of the data structure.

* Confluently persistent: can use combinators to combine input of more than one previous version to output a new single version.

* Functional persistent: never modify anything, only make new nodes. In a purely functional program all data is immutable, so all data structures are automatically fully persistent.

This class contains general techniques to do partial persistence and full persistence, and what we know about confluent persistence and functional persistence, which means 
the research related to the latter two persistence is not fully solved.

## Partially persistence  
The method that Eric shows is basically the node-copying method in the original paper [1]. 
This allows nodes in the persistent structure to hold only a fixed number of field values. 
When we run out of space in a node, we create a new copy of the node and update a set of back-pointers (up to *p* back-pointers, therefore at most *p* in-nodes).
We must also store pointers to the new copy in all predecessors of the copied node in the newest version. 
Therefore, the cost is recursive because of this field update for all predecessors. Here I will follow the partial persistence version in Eric's class.

**Partial persistence**: Any pointer-machine data structure with <= p = O(1) pointers to any node can be made partially persistent with O(1) amorized factor over head 
plus O(1) space.

The proof employs amortized analysis and potential method. The potential function $\Phi$ is defined as $\Phi = c\sum #mods$. 
Therefore whenever a recursion modification happens, the potential decrease (-2cp) cancels out with the $p\dot recursion$, very clever!

## Reference

[1] Driscoll, James R., et al. "Making data structures persistent." Proceedings of the eighteenth annual ACM symposium on Theory of computing. ACM, 1986.  

[2] Persistent data structure, https://en.wikipedia.org/wiki/Persistent_data_structure.
