# The Concept Graph

The notion of a concept graph will be build up step by step through a series of DIPs. Summary of the logic: (work in progress)

See a list of [important concepts](importantConcepts.md).

## prerequisites

- [DIP-03](../03.md): Representation of a graph using simple lists.

## DIPS 100-199: the Concept Graph

There will be a natural progression from simple lists, to complex lists, to concepts, to the concept graph.

- [DIP-100](100.md): simple list

- [DIP-101](101.md): complex list: a simple list with added structure

- [DIP-102](102.md): concept

- [DIP-103](103.md): concept graph

- [DIP-104](104.md): words and wordTypes 

- [DIP-105](105.md): publication of a word over nostr


# construction

maybe move word, wordType to DIP-100? then define lists (simple and complex) & list items, endorsements, etc as derivates of the notion of a word?

Currently a word is defined and specified in DIP-104; ought to move this to its own NIP and perhaps reorder some of them (move `publication of a word over nostr` to a later DIP, after `structure of a word`)

23 May: DIPs-104, 106 have been reassigned; need to make sure changes are propageted throughout this repo

Consider reorganizing as follows:
- 100 900 words
- 101 905 simple publication of a word over nostr
- 102 900b wordTypes
- 103 903 new wordType: relationship
- 104 903b new wordType: relationshipType
- 105 908 new wordType: graph (formerly called: schema)
- 106 902 new wordType: list
- 107 901 new wordType: jsonSchema
- 108 904 new wordType: set
- 109 904b new wordType: superset
- 110 906 class thread
- 111 907 new wordType: concept
- 112 909 new wordType: concept graph
- 113 910 new wordType: property

drafts not yet made
- how a user can publish a graph
- 9** where to find latest conceptGraph

publish in grapevine:
- 200 new wordTypes: attestation, endorsement, rating (place under grapevine?)
- 201 publication of an attestation, endorsement, rating over nostr (place under grapevine?)

# NOT YET ADDED:


- [DIP-10*](10*.md): use of graphs to represent complex lists and other data structures

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
