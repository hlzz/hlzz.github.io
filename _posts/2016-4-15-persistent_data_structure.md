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
This allows nodes in the persistent structure to hold only a fixed number of field values (*2p* where *p* is the maximum in-degree). 
When we run out of space in a node, we create a new copy of the node and update a set of back-pointers (up to *p* back-pointers, therefore at most *p* in-nodes).
We must also store pointers to the new copy in all predecessors of the copied node in the newest version. The *mod* is of the form (version, field, value)
Therefore, the cost is recursive because of this field update for all predecessors. Here I will follow the partial persistence version in Eric's class.

**Partial persistence**: Any pointer-machine data structure with <= p = O(1) pointers to any node can be made partially persistent with O(1) amorized factor over head 
plus O(1) space.

**Proof**: The proof employs amortized analysis and potential method. There are two cases for modifying the field value: 
The potential function $\Phi$ is defined as $\Phi = c\sum #mods$. 

* 1) If the node is not full (a node can store up to *2p* mods), just record the mod, so the amortized cost is c + c (the actual cost plus the potential increase)

* 2) If the node is full, make a new node and apply all the mods, update back pointers of the new node using the backpointers of the copied node, and recursively 
update pointers of the predecessors. 

Whenever a recursion modification happens, the potential decrease (-2cp) cancels out with the $p \dot recursion$, thus the amortized cost is constant. Very clever!

## Full persistence
Full persistence relies on a order-maintenance data structure in the future lecture, so that we can linearize a version tree by traversing the node:

* It can insert item before/after a given node in O(1) time.  

* Moreover, relative order of two item x&y can be answered in O(1) time.  

* "Is version *v* is an ancestor of *w*?" (b_v < b_w < e_w < e_v) can also be answered in O(1) time.  

To read node.field at version v we now need to look at the mods that are the nearest ancestor to v. The full persistence theorem does not change too much: 

**Full persistence**: Any pointer-machine data structure with <= p = O(1) pointers to any node can be made full persistent with O(1) amorized factor over head 
plus O(1) space.

Now we need to store back-pointers for all versions. A node can store up to *2(d+p+1)* mods, where *d* is the maximum out-degree and *p* is the maximum in-degree.
The update step is different from the partial persistence when the node is full. The old node is splitted into two nodes and then update pointers. 
In this case, the version tree should also be splitted at this point and some of the pointers that points to the original nodes should now point to the new node. 
So we need to recursively update *2d+2p+1* pointers. The potential function is $c\sum #empty mods. slots$. 
The following analysis is similar to the partially persistence case and omitted.  

De-amortize (Eric): O(1) worst-case slow down for partial persistence. For full persistent it is a open problem

## Confluent persistence and functional persistence
For confluent persistence the versions forms a DAG. [3] gives an exponential reduction in space and time compared to the naive method. 
I don't fully understand this part and there are still some open problems. 
So I will just list the literatures [3, 4, 5] that Eric has mentioned in his class for further reference.

## Reference

[1] Driscoll, James R., et al. "Making data structures persistent." Proceedings of the eighteenth annual ACM symposium on Theory of computing. ACM, 1986.  

[2] Persistent data structure, https://en.wikipedia.org/wiki/Persistent_data_structure.

[3] Fiat, Amos, and Haim Kaplan. "Making data structures confluently persistent." Proceedings of the twelfth annual ACM-SIAM symposium on Discrete algorithms. Society for Industrial and Applied Mathematics, 2001.

[4] Collette, Sébastien, John Iacono, and Stefan Langerman. "Confluent persistence revisited." Proceedings of the twenty-third annual ACM-SIAM symposium on Discrete Algorithms. SIAM, 2012.

[5] Okasaki, Chris. Purely functional data structures. Cambridge University Press, 1999