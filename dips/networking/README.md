Data Storage and Retrieval
=====

A data storage system needs to have a convention for unique identifiers of words

## [nostr](nostr)

For nostr we have: the event id used to publish a word (immutable), the steward pubkey + slug. All versions are theoretically available if you publish to 99xx (instead of 399xx).

## [IPFS](ipfs)

For IPFS we have: ipfs hash (immutable), ipns name (mutable); peerID is responsible for updating ipns with the most recent ipfs. All versions of a word are available if you know the ipfs hash of older versions.

## comparison

A single peerID can handle any number of concept graphs. A single nostr steward pubkey by convention should handle only one concept graph, so that slugs do not collide. 