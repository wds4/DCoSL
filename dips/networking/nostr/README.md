Data storage & retrieval: nostr
=====
How to use nostr to store and retrieve data (nodes, words) efficiently and effectively
-----

DIPs 1100-1109

Move all NIPs that are nostr related to this folder. Want to make it clear that DCoSL is independent of nostr, even though they do work well together.

## Concept Graph-specific

- [DIP-1100](1100.md): what goes into wordData.metaData.nostr
- [DIP-1101](1101.md): publication of a word over nostr
- [DIP-1102](1102.md): retrieval of a word from the nostr network
- [DIP-1103](1103.md): stewardship

## Grapevine-specific

- [DIP-1104](1104.md): publication of an attestation over nostr
- [DIP-1105](1105.md): alternate formatting and publication over nostr using [NIP-32](https://github.com/staab/nips/blob/nip-32-labeling/32.md)

## Work in progress

Divide publication to nostr into multiple DIPs. Each publication method has its own task slug and uses its own set of tags, to assist in retrieval of data. For example: createInstance allows you to put the name of the parent list or parent concept in a tag, to make it easier to search for all items on that parricular list or concept.

- createWord: publish a word (simplest)
- createInstance: publish a word as an item (= an instance) on a particular list. 
