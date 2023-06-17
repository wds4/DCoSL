# Declaration of `relationship`

## Declaration

```json
{
  "wordData": {
    "slug": "relationship",
    "wordTypes": ["wordType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "relationship"
        }
      }
    }
  },
  "wordTypeData": {
    "slug": "relationship",
    "name": "relationship",
    "title": "Relationship",
    "description": "A edge bwtween two nodes in a graph, as specified according to the DCoSL protocol."
  }
}
```

Alternate convention:
A universal unique identifier, in this case the nostr event id corresponding to the relevant declaration, is used in place of the slug + 'Data'.
- `wordData` is replaced by `4a5517d25ebae34b9794f1b8d4dba0681f7ff7297bacbc29de2c915695c53bfe` (see the [declaration of word](word.md))
- `wordTypeData` is replaced by `eb36f4e459500234538daaed36fcdcdf3b7f0ee8912959da5ad10053725f6b28` (see the [declaration of word type](word.md))


```json
{
  "4a5517d25ebae34b9794f1b8d4dba0681f7ff7297bacbc29de2c915695c53bfe": {
    "slug": "relationship",
    "wordTypes": ["wordType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "relationship"
        }
      }
    }
  },
  "eb36f4e459500234538daaed36fcdcdf3b7f0ee8912959da5ad10053725f6b28": {
    "slug": "relationship",
    "name": "relationship",
    "title": "Relationship",
    "description": "A edge bwtween two nodes in a graph, as specified according to the DCoSL protocol."
  }
}
```

## Publication to nostr

as per [DIP-901](../../networking/nostr/901.md)

```json

```

## Retrieval from nostr

As per DIP 101 (updated for testnet-2), all versions of the above word can be found in nostr (testnet-2) using the following filter:

```json
{
  "since": 0,
  "kinds": [9902],
  "authors": ["c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"],
  "#c": ["concept-graph-testnet-902"],
  "#w": [""],
}
```

or

```json
{
  "ids": [""],
}
```

## References

- `relationship` is introduced in [DIP-103](../103.md).
- glossary entry: [relationship](../../../glossary/relationship.md), [word type](../../../glossary/wordType.md)
