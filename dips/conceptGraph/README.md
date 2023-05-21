# The Concept Graph

## Important Concepts

### the special utility for graphs (and graph databases) in DCoSL

It would be difficult to overstate the importance of graphs in DCoSL. A graph is a collection of nodes and edges. In DCoSL, a node generally is a file (often formatted using JSON), referenced by a crytographic identifier (DIP02), with edges relationships between the data. Crowdsourcing of complex things like data models, schemas, etc are easiest to understand in terms of a graph. Web of trust is best visualized using a graph.

A graph is a collection of nodes and edges, with each edge being a connection between two nodes. A graph can therefore be specified in full using no more than <i>two simple lists</i>, each one of which can be managed using DCoSL! (May want to have a thid list for types of edges, and perhaps a fourth list for types of nodes. But in many cases those lists would be managed by the developer, leaving only two lists to be curated by the WoT.)

Graphs have the attractive quality that they can be combined using basic set operators: union, intersection, etc. So if my WoT approves of Graph A as well as Graph B, then Alice can combine Graphs A and B into Graph C through the union operation. Example: Graph A is Verifiable Credential backbone curated by users who specialize in Verifiable Credentials, and Graph B is an auxiliary Verifiable Credential for nurse practitioners, curated by users who are nurse practitioners, but which assumes the VC backbone to be curated separately.

In the DIPs that follow, several specialized graphs will be defined, each with specialized edge types and node types that are defined within the DIP.
<li>a graph for an individual Concept</li>
<li>a graph for the subset tree for a particular concept</li>
<li>a graph for the Property Tree which defines the JSON Schema for a concept</li>
<li>a layer 1 Concept Graph, which shows the high level relationships between multiple Concepts</li>
<li>a graph for a Context Tree, which is used by the grapevine to calculate context-based scores by inheritance of default values from generic contexts to specific contexts</li>

Each of the above types of graphs can be specified by the developer, can be managed by hand by the individual user, or can be farmed out to one's web of trust.

### Classes

DCoSL borrows the notion of a class from javascript and (most) other object oriented programming languages.

Consider a graph, with nodes and edges. The following terms will be defined:

`thread`: any contiguous sequence of edges. Must contain at least one edge.

`class thread`: a specialized thread, with a `class node` at the start and a `class instance` at the end

`class node`:

`class instance`:

`class thread rule`: the requirement that any class instance must be formatted according to rules specified by the class node. For example: if the class node User specifies properties: display_name and picture_url, then any class instance node must have those properties; otherwise the class thread rule is violated.

`class property tree`: 

A concept is defined as a collection of nodes and edges, formed from a single class node, taking all class threads emanating from that node (all nodes and edges contained within those threads). (Is property tree added to the definition of the concept?)

## important prerequisite

- [DIP-03](../03.md): Representation of a graph using simple lists.

## DIPS 100-199: the Concept Graph

There will be a natural progression from simple lists, to complex lists, to concepts, to the concept graph.

threads, class threads, class node, class instance; analogy to the class in object-oriented programming

nodes, edges (relationships)

basic types of nodes: JSONSchema, wordType, set, superset, instance

basic types of relationships: subsetOf, JSONSchemaFor, specificInstanceOf

the Loki Principle = class thread rule

thread; class thread; class thread rule (principle of Loki)

three basic relationships between concepts

use of graphs to represent complex lists and other data structures

use of graphs to represent data structures; use of cryptographic identifiers for nodes (and edges)

- [DIP-100](100.md): simple list

- [DIP-101](101.md): complex list: simple list with added structure

