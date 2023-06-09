# Declaration of `set`

## Declaration

```json
{
  "wordData": {
    "slug": "set",
    "wordTypes": ["wordType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "set"
        }
      }
    }
  },
  "wordTypeData": {
    "oSlug": {
      "singular": "set",
      "plural": "sets"
    },
    "oName": {
      "singular": "set",
      "plural": "sets"
    },
    "oTitle": {
      "singular": "Set",
      "plural": "Sets"
    },
    "propertyPath": "setData",
    "description": "As specified according to the DCoSL protocol."
  }
}
```

NOTE: the above word type (above) may not match the published version (below) due to editing subsequent to publishing.

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

- `set` is introduced in [DIP-??](../??.md).
- glossary entry: [set](../../../glossary/set.md), [word type](../../../glossary/wordType.md)

