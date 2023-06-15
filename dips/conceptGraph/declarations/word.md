# Declaration of `word`

## Declaration

```json
{
  "wordData": {
    "slug": "wordType_word",
    "name": "word type: word",
    "title": "Word Type: Word",
    "wordTypes": ["wordType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"
        "uniqueIDs": {
          "slug": "wordType_word"
        }
      }
    }
  },
  "wordTypeData": {
    "slug": "word",
    "name": "word",
    "title": "word",
    "description": "A node in a graph, formatted in json, with additional requirements specified in DIP-100"
  }
}
```

## Publication to nostr

```json
```


As per DIP 101 (updated for testnet-2), all versions of the above word can be found in nostr (testnet-2) using the following filter:

```json
{
  "since": 0,
  "kinds": [9902],
  "authors": ["c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"],
  "tags": [
    "#c": ["concept-graph-testnet-902"],
    "#w": ["wordType_word"],
  ]
}
```

## References

- `word` is introduced in [DIP-100](../100.md).
- glossary entry: [word](../../../glossary/word.md), [word type](../../../glossary/wordType.md)
