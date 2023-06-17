# Declaration of `nostr curated list`

## Declaration

```json
{
  "wordData": {
    "slug": "nostrCuratedList",
    "wordTypes": ["wordType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "nostrCuratedList"
        }
      }
    }
  },
  "wordTypeData": {
    "oSlug": {
      "singular": "nostrCuratedList",
      "plural": "nostrCuratedLists"
    },
    "oName": {
      "singular": "nostr curated list",
      "plural": "nostr curated lists"
    },
    "oTitle": {
      "singular": "Nostr Curated List",
      "plural": "Nostr Curated Lists"
    },
    "description": "A list that is created according to the DCoSL protocol."
  }
}
```

NOTE: the above word type (above) may not match the published version (below) due to editing subsequent to publishing.

## Publication to nostr

as per [DIP-1101](../../networking/nostr/1101.md)

```json
{
    "id": "50e65e129b6edc8f30c0160f64b7ce0175d7e6bb75b64ae0e4c5db1384979a82",
    "pubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
    "created_at": 1686900356,
    "kind": 9902,
    "tags": [
        [
            "c",
            "concept-graph-testnet-2"
        ],
        [
            "t",
            "createWord"
        ],
        [
            "s",
            "word"
        ],
        [
            "w",
            "nostrCuratedList"
        ]
    ],
    "content": "{\"wordData\":{\"slug\":\"nostrCuratedList\",\"wordTypes\":[\"wordType\"],\"metaData\":{\"nostr\":{\"stewardPubkey\":\"c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa\",\"uniqueIDs\":{\"slug\":\"nostrCuratedList\"}}}},\"wordTypeData\":{\"slug\":\"nostrCuratedList\",\"name\":\"nostr curated list\",\"title\":\"Nostr Curated List\",\"description\":\"A list that is created according to the DCoSL protocol.\"}}",
    "sig": "6e20eda718ad516867fb2e7ddcc8640b243fc57b096e5ee9202e1137c9edee97271f0076e18deafcebc2f5c4890b8798023f276e9778eb76dcc1eb5b2bcab43c"
}
```

## Retrieval from nostr

As per DIP 101 (updated for testnet-2), all versions of the above word can be found in nostr (testnet-2) using the following filter:

```json
{
  "since": 0,
  "kinds": [9902],
  "authors": ["c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"],
  "#c": ["concept-graph-testnet-902"],
  "#w": ["list"],
}
```

or

```json
{
  "ids": ["50e65e129b6edc8f30c0160f64b7ce0175d7e6bb75b64ae0e4c5db1384979a82"],
}
```

## References

- relevant glossary entry: [word type](../../../glossary/wordType.md)
