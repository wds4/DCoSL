hybrids
=====

Hybrids are words that are a mixture of several words together. 

## augmented lists: hybrid `wordType` and `jsonSchema`

One useful combination is `wordType` plus `jsonSchema`, which has more functionallity than a basic list but not the full funcionality of a concept. Basically any simple list that you really wish you could augment with some extra fields.

Example uses:

nostr content curation requires several augmented lists.

A list of nostr content categories, each of which has a name and a description (a simple list)

a list of relationships. Each item is a relationship between two categories which requires two fields:
- one for category 1
- one for category 2

An array of list of pubkeys which provide great content on category X. Each of these lists requires
- name
- the category, which could be a bespoke field of its own or could just go into the description field
These lists will be created automatically, one for each new category that gets created. Will these lists need to be declared formally? Not sure. Hopefullly not.

Endorsements of curators 
