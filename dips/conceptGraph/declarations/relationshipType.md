# Declaration of `relationship type`

## Declaration

```json
{
  "wordData": {
    "slug": "relationshipType",
    "wordTypes": ["wordType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "relationshipType"
        }
      }
    }
  },
  "wordTypeData": {
    "oSlug": {
      "singular": "relationshipType",
      "plural": "relationshipTypes"
    },
    "oName": {
      "singular": "relationship type",
      "plural": "relationship types"
    },
    "oTitle": {
      "singular": "Relationship Type",
      "plural": "Relationship Types"
    },
    "propertyPath": "relationshipTypeData",
    "description": "A category of relationships, as specified according to the DCoSL protocol."
  }
}
```

NOTE: the above word type (above) may not match the published version (below) due to editing subsequent to publishing.

## Publication to nostr

as per [DIP-1101](../../networking/nostr/1101.md)

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

- `relationship type` is introduced in [DIP-104](../104.md).
- glossary entries: [relationship type](../../../glossary/relationshipType.md), [word type](../../../glossary/wordType.md)
