Data Storage and Retrieval: DIPs 1000-1999
=====

This series of DIPs addresses various methods to store and retrieve data from various networks. Nodes and words are as defined in the relevant DIPs.

A data storage system needs to have a convention for unique identifiers of words

## DIPs 1000-1099: integration of new networks with DCoSL

The DCoSL protocol, outside of these DIPs, is intended to be agnostic of how and where the data is stored. Methods for initiating the process of integration or adoption of new a network or storage system are discussed in this section of DIPs. Once initial integration is specified 

The most important issue is that data needs a method for lookup and identification that is unique. It is recommended that identifiers be universally unique, such as the eventID for nostr or the ipfs hash or ipns name for ipfs network.

New networks can be assigned DIP numbers in blocks of 10. More can be reserved if desired.

## [nostr](nostr): DIPs 1100-1110

For nostr we have: the event id used to publish a word (immutable), the steward pubkey + slug. All versions are theoretically available if you publish to 99xx (instead of 399xx).

## [IPFS](ipfs): DIPs 1111-1120

For IPFS we have: ipfs hash (immutable), ipns name (mutable); peerID is responsible for updating ipns with the most recent ipfs. All versions of a word are available if you know the ipfs hash of older versions.

## comparison

A single peerID can handle any number of concept graphs. A single nostr steward pubkey by convention should handle only one concept graph, so that slugs do not collide. 
