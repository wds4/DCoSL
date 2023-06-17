# The Concept Graph

In DCoSL, data is represented as a [graph](../../glossary/graph.md), with [nodes](../../glossary/node.md) and [edges](../../glossary/relationship.md). A concept graph is a graph with additional structure, as described though this series of DIPs.

A [simple list](../../glossary/simpleList.md) will be defined (in [DIP-106](106.md)) as a node with particular characteristics. The idea of a simple list will then mature into the notion of a [concept](../../glossary/concept.md) ([DIP-111](111.md)).

See a list of [important concepts](importantConcepts.md).

## prerequisites

- [DIP-03](../coreProtocol/03.md): Representation of a graph using simple lists.

## DIPS 100-199: the Concept Graph

There will be a natural progression from simple lists, to complex lists, to concepts, to the concept graph.

Note: the numeric designation of these DIPs is subject to change.

WORDS: (100-109)
- (100) [DIP-100](100.md): word
- (101) [DIP-102](102.md): word types 
- (102) [DIP-102b](102b.md): local identifiers: slug, name, title 
- (103) maybe combine 100b and 100c into: networks, universal identifiers, and metaData. (link to network/nostr and network/ipfs)

might deprecate these
- [DIP-100b](100b.md): unique word identifiers
- [DIP-100c](100c.md): unique word identifier types


maybe start here at 110 with WORD TYPES
- (110) [DIP-103](103.md): relationships
- (111) [DIP-104](104.md): relationship types
- [DIP-105](105.md): graphs
- [DIP-106](106.md): lists
- [DIP-107](107.md): json schemas
- [DIP-108](108.md): sets
- [DIP-109](109.md): supersets
- [DIP-111](111.md): concepts
- [DIP-112](112.md): concept graphs
- [DIP-113](113.md): properties
- [DIP-114](114.md): graph types
- item directory - a type of graph will the superset, all relevant sets, and all items for a given concept (what I used to call a schema)
- property directory - a type of graph with all relevant properties for a given concept (what I used to call a propertySchema)

start here at 130?
- [DIP-110](110.md): class threads


  
# under construction

drafts in progress
- [DIP-190](190.md): concept graph nostr publication tasks


drafts not yet made
- declaration of a new concept
- 901: context tree
- how a user can publish a graph
- public archives for a dictionary?
- graph types: generic type, 
- 90*: publish or pin a list of words (graph, concept graph, dictionary?)
- 90*: conventions for cryptographic identifiers (wordData vs metaData, mutable vs immutable, IPNS name vs ... ?)
- 90*: graphical representation of a concept
- 90*: graphical representation of a property tree
- 90*: graphical representation of schemas
- 90*: graphical representation of JSON-LD
- 90*: graphical representation of data model

publish in grapevine:
- 200 new wordType: attestation
- 201 new wordType: endorsement
- 202 new wordType: rating
- 203 publication of an attestation, endorsement, rating over nostr


