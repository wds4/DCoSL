Declaration of `word`
=====

## Declaration

as per [DIP-102](../102.md)

```json
{
  "wordData": {
    "slug": "word",
    "wordTypes": ["wordType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "word"
        }
      }
    }
  },
  "wordTypeData": {
    "slug": "word",
    "name": "word",
    "title": "Word",
    "description": "A node in a graph, formatted in json, with additional requirements and conventions specified according to the DCoSL protocol."
  }
}
```

(above has been edited and may not match the below)

## Publication to nostr

as per [DIP-901](../../networking/nostr/901.md)

```json
{
    "id": "4a5517d25ebae34b9794f1b8d4dba0681f7ff7297bacbc29de2c915695c53bfe",
    "pubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
    "created_at": 1686887272,
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
            "word"
        ]
    ],
    "content": "{\"wordData\":{\"slug\":\"word\",\"name\":\"word\",\"title\":\"Word\",\"wordTypes\":[\"wordType\"],\"metaData\":{\"nostr\":{\"stewardPubkey\":\"c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa\",\"uniqueIDs\":{\"slug\":\"word\"}}}},\"wordTypeData\":{\"slug\":\"word\",\"name\":\"word\",\"title\":\"word\",\"description\":\"A node in a graph, formatted in json, with additional requirements and conventions specified according to the DCoSL protocol.\"}}",
    "sig": "f3925f65a397f5a9d221f7305ca9e67eb491fc0ceeacef8d8cbb3758b5f06bdd382aea606b4526986c2666c4d3d7f9d0518c696d8d85dc25a107846d2801eabf"
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
  "#w": ["word"],
}
```

or

```json
{
  "ids": ["4a5517d25ebae34b9794f1b8d4dba0681f7ff7297bacbc29de2c915695c53bfe"],
}
```

## References

- `word` is introduced in [DIP-100](../100.md).
- glossary entry: [word](../../../glossary/word.md), [word type](../../../glossary/wordType.md)
