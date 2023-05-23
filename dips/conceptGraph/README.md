# The Concept Graph

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
- 100 words and wordTypes
- 101 new wordType: jsonSchema
- 102 new wordType: lists
- 103 new wordType: relationships, relationshipTypes

# NOT YET ADDED:

- [DIP-10*](10*.md): JSONSchemas

- [DIP-10*](10*.md): implementation as a graph database

- [DIP-10*](10*.md): class

- [DIP-10*](10*.md): class threads

analogy to the class in object-oriented programming

threads, class threads, class node, class instance, class thread rule

- [DIP-10*](10*.md): use of graphs to represent complex lists and other data structures

- [DIP-10*](10*.md): graphical representation of a concept

- [DIP-10*](10*.md): graphical representation of a property tree

- [DIP-10*](10*.md): graphical representation of a context tree

- [DIP-10*](10*.md): graphical representation of schemas

- [DIP-10*](10*.md): graphical representation of JSON-LD

- [DIP-10*](10*.md): graphical representation of data model



