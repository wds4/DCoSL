threaded tapestry
=====

The `threaded tapestry` model is a proposed model of [knowledge representation](knowledgeRepresentation.md) and [knowledge curation](knowledgeCuration.md) for a [decentralized, distributed system](decentralizedDistributedSystem.md) such as the decentralized web or the cortex. It is designed to solve one of the chief problems faced by such networks: how to develop and manage a common language, without which no network can properly function, without the need to place any single entity in charge of the network.

### overview

In the threaded tapestry model, information is represented as a graph database. A specialized path called a [class thread](classThread.md) is employed as a central tool for organization of information into [concepts](concept.md), comparable in some ways to the way that a [class](class.md) is used to organize objects in many object oriented programming languages.

### more detailed presentation of the TT model

Two examples will be used to elaborate on the TT model: the decentralized web model (name for this?) and the cortical tapestry model.

The starting point is the `graph database` model. According to the graph database model, information is represented in a graph using three distinct formats:
- within each node
- within each edge
- within the topology of the graph

One of the presumptions is that the amount of information stored within an edge is kept to a minimum. Relativelhy speacking, an individual node should store, on average, more infotmation than an individual edge. In our CS example (neo4), this is the case: edges have a few properties but not many, while nodes are commonly files and can be of unlimited size, as large (or as small) as is required.

The cortical graph database hypothesis (better name for this?) is the hypothesis that the graph database model applies to the brain. Although the phrase itself is not necessarily a part of the academic literature, the content of the CGDH is not terribly controversial. The questions at hand would be: what are the nodes and what are the edges? Indeed, the hypothesis itself is arguably not very substantive without specifying those physical substrates. I offer two variations: the first and most obvious would be nodes are neurons and edges are axonal (and/or dendritic) projections. But I prefer the second, which is that nodes are cortical columns. (And edges are axonal and dendritic connections between columns.)

The main question: how is information formatted, or represented?

According to the threaded tapestry model, the graph databse is subject to a small handful of major and minor `criteria`. The first and most important of the criteria is the `class thread criterion` (need a better name for this), according to which: for any class thread, the node at the beginning of the thread is an element of the node at the end of the thread. 

It is assumed that background processing / housekeeping algorithms must exist to ensure enforcement of the various criteria, and that the amount of processing power required to run these algorithms is of central importance in understanding how the cortex is structured, bc they must be optimized to maximize efficiency. In some circumstances, the class thread criterion is violated. Most notably, this may be seen to occur in `toxic threads`, but it can happen in other circumstances as well.

