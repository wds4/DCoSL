# The Concept Graph

## Important Concepts

### the special utility for graphs (and graph databases) in DCoSL

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

## DIPS 100-199: the Concept Graph

There will be a natural progression from simple lists, to complex lists, to concepts, to the concept graph.

threads, class threads, class node, class instance; analogy to the class in object-oriented programming

nodes, edges (relationships)
basic types of nodes: JSONSchema, wordType, set, superset, instance
basic types of relationships: subsetOf, JSONSchemaFor, specificInstanceOf
the Loki Principle = class thread rule

thread; class thread; class thread rule (principle of Loki)

three basic relationships between concepts

- [DIP-100](100.md): basic use of graphs

use of graphs to represent complex lists and other data structures
use of graphs to represent data structures; use of cryptographic identifiers for nodes (and edges)

- [DIP-101](101.md): complex lists

parent list augmented by auxiliary lists
subsets, subset trees, properties, property trees
