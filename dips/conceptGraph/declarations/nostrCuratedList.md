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
    "slug": "nostrCuratedList",
    "name": "nostr curated list",
    "title": "Nostr Curated List",
    "description": "A list that is created according to the DCoSL protocol."
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
  "#w": ["list"],
}
```

or

```json
{
  "ids": [""],
}
```

## References

- relevant glossary entry: [word type](../../../glossary/wordType.md)
