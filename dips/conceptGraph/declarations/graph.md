# Declaration of `graph`

## Declaration

```json
{
  "wordData": {
    "slug": "graph",
    "wordTypes": ["wordType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "graph"
        }
      }
    }
  },
  "wordTypeData": {
    "slug": "graph",
    "oName": {
      "singular": "graph",
      "plural": "graphs"
    },
    "oTitle": {
      "singular": "Graph",
      "plural": "Graphs"
    },
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

- `graph` is introduced in [DIP-105](../105.md).
- relevant glossary entries: [graph](../../../glossary/graph.md), [word type](../../../glossary/wordType.md)
