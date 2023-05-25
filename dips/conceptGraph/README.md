# The Concept Graph

The notion of a concept graph will be build up step by step through a series of DIPs. Summary of the logic: (work in progress)

See a list of [important concepts](importantConcepts.md).

## prerequisites

- [DIP-03](../03.md): Representation of a graph using simple lists.

## DIPS 100-199: the Concept Graph

There will be a natural progression from simple lists, to complex lists, to concepts, to the concept graph.

- [DIP-100](100.md): words
- [DIP-101](101.md): publication of a word over nostr
- [DIP-102](102.md): word types
- [DIP-103](103.md): relationships
- [DIP-104](104.md): relationship types
- [DIP-105](105.md): graphs
- [DIP-106](106.md): lists
- [DIP-107](107.md): json schemas
- [DIP-108](108.md): sets
- [DIP-109](109.md): supersets
- [DIP-110](110.md): class threads
- [DIP-111](111.md): concepts
- [DIP-112](112.md): concept graphs
- [DIP-113](113.md): properties

# works in progress - notes

drafts not yet made
- 900: publish or pin a list of words (graph, concept graph, dictionary?)
- 901: conventions for cryptographic identifiers (wordData vs metaData)

- how a user can publish a graph
- public archives for a dictionary?
 
publish in grapevine:
- 200 new wordTypes: attestation, endorsement, rating (place under grapevine?)
- 201 publication of an attestation, endorsement, rating over nostr (place under grapevine?)

# NOT YET ADDED:

- [DIP-10*](10*.md): graphical representation of a concept

- [DIP-10*](10*.md): graphical representation of a property tree

- [DIP-10*](10*.md): graphical representation of a context tree

- [DIP-10*](10*.md): graphical representation of schemas

- [DIP-10*](10*.md): graphical representation of JSON-LD

- [DIP-10*](10*.md): graphical representation of data model

# Word types

| word type | top level property | definition |
| ----- | ----- | ----- |
| word | wordData | any node which represents an object |
| wordType | wordTypeData | |
| jsonSchema | jsonSchemaData | |
| superset | supersetData | |
| set | setData | |
| concept | conceptData | |
| graph | graphData | |

# Relationship types

| relationship type | nodeFrom | nodeTo |
| ----- | ----- | ----- |
| subsetOf | set | set |
