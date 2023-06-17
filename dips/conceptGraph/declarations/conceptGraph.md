# Declaration of `concept graph`

## Declaration

```json
{
  "wordData": {
    "slug": "conceptGraph",
    "wordTypes": ["wordType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "conceptGraph"
        }
      }
    }
  },
  "wordTypeData": {
    "slug": "conceptGraph",
    "name": "concept graph",
    "title": "Concept Graph",
    "description": "As specified according to the DCoSL protocol."
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

- `concept graph` is introduced in [DIP-112](../112.md).
- relevant glossary entries: [concept graph](../../../glossary/conceptGraph.md), [word type](../../../glossary/wordType.md)
