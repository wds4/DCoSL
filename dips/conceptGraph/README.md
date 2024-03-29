# The Concept Graph

STATUS OF THIS DOCUMENT: under construction

DIP-00: In DCoSL, data is represented as a [graph](../../glossary/graph.md), with [nodes](../../glossary/node.md) and [edges](../../glossary/relationship.md). A concept graph is a graph with additional structure, as described though this series of DIPs.

A [simple list](../../glossary/simpleList.md) (the SL in DCoSL) will be defined (in [DIP-106](106.md)) as a node with particular characteristics. The idea of a simple list will then mature into the notion of a [concept](../../glossary/concept.md) ([DIP-111](111.md)).

See a list of [important concepts](importantConcepts.md).

## DIPS 100-199: the Concept Graph

There will be a natural progression from simple lists, to complex lists, to concepts, to the concept graph.

Note: the numeric designation of these DIPs is subject to change.

GRAPH BASICS: words, relationships (100-109)
- [DIP-100](100.md): words
- [DIP-101](101.md): word types
- [DIP-102](102.md): local identifiers: slug, name, title
- [DIP-103](103.md): relationships
- [DIP-104](104.md): relationship types
- [DIP-105](105.md): graphs
- [DIP-106](106.md): lists

The nodes that make up CLASS THREADS (110-119)
- [DIP-110](110.md): json schemas
- [DIP-111](111.md): sets
- [DIP-112](112.md): supersets
- [DIP-113](113.md): class threads
- [DIP-114](114.md): hybrids
  
CONTAINERS, ORGANIZERS (start with 120-130) including CONCEPT GRAPH and rules

- [DIP-121](121.md): concepts
- [DIP-122](122.md): concept graphs
- [DIP-123](123.md): properties
- [DIP-124](124.md): graph types (may not need this?)
- [DIP-125](125.md): item directory
- [DIP-126](126.md): property directory - a type of graph with all relevant properties for a given concept (what I used to call a propertySchema)

# under construction

drafts in progress
- [DIP-190](190.md): concept graph nostr publication tasks -- move this to the 1100 block of DIPs

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

# May be deprecated
- [DIP-100b](100b.md): unique word identifiers
- [DIP-100c](100c.md): unique word identifier types
- (107) maybe combine 100b and 100c into: networks, universal identifiers, and metaData. (link to network/nostr and network/ipfs)
