another sample graph
=====

This is an alternate, more compact format for the `graph` word type. Different properties in `graphData` than in the first example. Not sure if I will make this a distinct graph format with a different name or just an alternate implementation of the `graph` concept.

`graphData.uniqueIdTypes` takes values: `nostrEventID` (typically), `nostrStewardPubkeyPlusSlug`, `ipfsHash`, `ipnsName`, or `slug`. If `slug` is indicated, then there must be a location to look up the word using the slug, typically within another graph; would need to decide how to specify the graph.

```json
{
  "wordData": {
    "slug": "anotherSampleGraph",
    "wordTypes": ["graph"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "sampleGraph"
        }
      }
    }
  },
  "graphData": {
    "slug": "sampleGraph",
    "uniqueIdTypes": ["nostrEventID"],
    "nodes": [
      "abcde12345",
      "bcdef23456"
    ],
    "relationships": [
      ["abcde12345","isASubsetOf","bcdef23456"]
    ],
  }
}
```