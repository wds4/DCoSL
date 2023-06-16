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
    "slug": "list",
    "name": "list",
    "title": "List",
    "description": "As specified according to the DCoSL protocol."
  }
}
```

## Publication to nostr

as per [DIP-101](../101.md)

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

- `list` is introduced in [DIP-106](../106.md).
- relevant glossary entries: [list](../../../glossary/list.md), [word type](../../../glossary/wordType.md)
