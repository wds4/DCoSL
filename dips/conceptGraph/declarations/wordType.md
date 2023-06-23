Declaration of `word type`
=====

## Declaration

New word types are declared as outlined in [DIP-102](../102.md).

```json
{
  "wordData": {
    "slug": "wordType",
    "version": "standard",
    "wordTypes": ["wordType"]
  },
  "wordTypeData": {
    "oSlug": {
      "singular": "wordType",
      "plural": "wordTypes"
    },
    "oName": {
      "singular": "word type",
      "plural": "word types"
    },
    "oTitle": {
      "singular": "Word Type",
      "plural": "Word Types"
    },
    "propertyPath": "wordTypeData",
    "description": "A category of word, as specified by the DCoSL protocol. The creation of a word of type: wordType is the primary method for declaration of a new list or concept."
  }
}
```

NOTE: the above word type (above) may not match the published version (below) due to editing subsequent to publishing.

## Publication to nostr

as per [DIP-1101](../../networking/nostr/1101.md)

```json
{
    "content": "{\"wordData\":{\"slug\":\"wordType\",\"wordTypes\":[\"wordType\"],\"metaData\":{\"nostr\":{\"stewardPubkey\":\"c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa\",\"uniqueIDs\":{\"slug\":\"wordType\"}}}},\"wordTypeData\":{\"slug\":\"wordType\",\"name\":\"word type\",\"title\":\"Word Type\",\"description\":\"A category of word, as specified by the DCoSL protocol. The creation of a word of type: wordType is the primary method for declaration of a new list or concept.\"}}",
    "created_at": 1686888769,
    "id": "eb36f4e459500234538daaed36fcdcdf3b7f0ee8912959da5ad10053725f6b28",
    "kind": 9902,
    "pubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
    "sig": "9180a3b351d4d445305da964f90b093850b52412cfe9150bf678c6bba2a13d3964c0a5ed22df7e53f6a42a56d6872169986a557ece96c483338988e2d8eecf3c",
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
            "wordType"
        ]
    ]
}
```

## Retrieval from nostr

As per [DIP-902](../../networking/nostr/902.md) (updated for testnet-2), all versions of the above word can be found in nostr (testnet-2) using the following filter:

```json
{
  "since": 0,
  "kinds": [9902],
  "authors": ["c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"],
  "#c": ["concept-graph-testnet-2"],
  "#w": ["wordType"],
}
```

or

```json
{
  "ids": ["eb36f4e459500234538daaed36fcdcdf3b7f0ee8912959da5ad10053725f6b28"],
}
```

## References

- `word type` is introduced in [DIP-102](../102.md).
- glossary entry: [word type](../../../glossary/wordType.md)
