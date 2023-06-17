# Declaration of `list`

## Declaration

```json
{
  "wordData": {
    "slug": "list",
    "wordTypes": ["wordType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "list"
        }
      }
    }
  },
  "wordTypeData": {
    "oSlug": {
      "singular": "list",
      "plural": "lists"
    },
    "oName": {
      "singular": "list",
      "plural": "lists"
    },
    "oTitle": {
      "singular": "List",
      "plural": "Lists"
    },
    "description": "As specified according to the DCoSL protocol."
  }
}
```

NOTE: the above word type (above) may not match the published version (below) due to editing subsequent to publishing.

## Publication to nostr

as per [DIP-901](../../networking/nostr/901.md)

```json
{
    "content": "{\"wordData\":{\"slug\":\"list\",\"wordTypes\":[\"wordType\"],\"metaData\":{\"nostr\":{\"stewardPubkey\":\"c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa\",\"uniqueIDs\":{\"slug\":\"list\"}}}},\"wordTypeData\":{\"slug\":\"list\",\"name\":\"list\",\"title\":\"List\",\"description\":\"As specified according to the DCoSL protocol.\"}}",
    "created_at": 1686899929,
    "id": "f8a0813f4be715aa29a8904479809061136c5f7834e09d514d083fa43c6e14d6",
    "kind": 9902,
    "pubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
    "sig": "6a6b3fadee4e0ebfab831e1e23109c56bbaf2f6b5212a4e0ea7d6e2d0366448c2f68810219648b69097f2b17a23c8c72345bf7e3f1a3ad632f64a279039871e6",
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
            "list"
        ]
    ]
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
  "ids": ["f8a0813f4be715aa29a8904479809061136c5f7834e09d514d083fa43c6e14d6"],
}
```

## References

- `list` is introduced in [DIP-106](../106.md).
- relevant glossary entries: [list](../../../glossary/list.md), [word type](../../../glossary/wordType.md)
