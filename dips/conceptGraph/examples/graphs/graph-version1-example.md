sample graph (version 1 format)
=====

Note that the word below validates against the json schema for graphs, [version 1](https://github.com/wds4/DCoSL/blob/main/dips/conceptGraph/examples/jsonSchemas/graph-version1.md) but not [version 2](https://github.com/wds4/DCoSL/blob/main/dips/conceptGraph/examples/jsonSchemas/graph-version2.md).

```json
{
  "wordData": {
    "slug": "sampleVersion2Graph",
    "wordTypes": ["graph"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "sampleVersion2Graph"
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
