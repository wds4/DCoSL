Data Storage and Retrieval: DIPs 1000-1999
=====

This series of DIPs addresses various methods to store and retrieve data from various networks. Mostly concerned with data content addressing and how / where to put it in a word.

## Background

The DCoSL protocol, outside of these DIPs, is intended to be agnostic of how and where the data is stored. New networks are encouraged. Multiple networks can be used simultaneously within a single word or concept graph. The more systems that are utilized, the more robust and DCoSL will become, the more difficult it will be to fall under the control of any single entity. It may turn out that different networks may have distinct utilities: nostr for smaller files (text only), another for larger files (ipfs for nodes that correspond to images and video), etc.

References to specific data networks, although not avoided completely, are kept to a minimum in all DIPs below 1000. Methods for initiating the process of integration or adoption of new a network or storage system are discussed in this section of DIPs.

The most important issue is that data needs one or more methods for lookup and identification that is unique. It is recommended that identifiers be universally unique, such as the eventID for nostr or the ipfs hash or ipns name for ipfs network. This will obviate the need for any single entity to manage the list of identifiers and will prevent the problem of "domain squatting" that plagues URLs within the domain name system (DNS)

The system that works for nostr, and may work for other networks, is to have:
- one universally unique identifier for each data chunk
- one identifier that is intented to be unique within some local system, but not globally
- universally unique identifier corresponding to an author, curator, or steward, who then has some author-especific system for content identification, e.g. for nostr: pubkey + slug

## [DIPs 1000-1099: individual network introductions](networkIntroductions)

To initiate a new network:
- a single introductory DIP in the range: 1000-1099 outlining the rationale for using this network and possibly outlining the system of identifiers 
- assign a block of DIP numbers somewhere in 1100-1999, typically in blocks of 10. More can be reserved if desired.

Typically, a `slug` corresponding to the new network in question will be chosen for addressing inside `wordData.metaData` as follows:

```json
{
  "wordData": {
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "fooBar",
          "version": "alternate"
        }
      },
      "ipfs": {
        "stewardPeerID": null,
        "uniqueIDs": {
          "ipns": null,
          "ipfs": null,
          "slug": "fooBar",
          "version": "alternate"
        }
      }
      "[slug for new network solution]": {
        ...
      }
    }
  },
  ...
}
```

## [nostr: DIPs 1100-1110](nostr)

For nostr we have: the event id used to publish a word (immutable), the steward pubkey + slug. All versions are theoretically available if you publish to 99xx (instead of 399xx).

## [IPFS: DIPs 1111-1120](ipfs)

For IPFS we have: ipfs hash (immutable), ipns name (mutable); peerID is responsible for updating ipns with the most recent ipfs. All versions of a word are available if you know the ipfs hash of older versions.

## comparison

A single peerID can handle any number of concept graphs. A single nostr steward pubkey by convention should handle only one concept graph, so that slugs do not collide. 
