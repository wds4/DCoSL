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
        "lookup": "npub1ya43wd06ugax6vjgnguqgeah0xtkg5mpwr5jg5gznhk3cz53jzzqfftu4x:wordType_word",
        "stewardPubkey": "npub1ya43wd06ugax6vjgnguqgeah0xtkg5mpwr5jg5gznhk3cz53jzzqfftu4x", 
      },
    },
  },
  "wordTypeData": {
    "slug": "word",
    "name": "word",
    "title": "word",
    "description": "A node in a graph, formatted in json, with additional requirements specified in DIP-100",
  },
}
```

As per DIP 101, all versions of the above word can be found in nostr (testnet-1) using the following filter:

```json
{
  "since": 0,
  "kinds": [9901],
  "authors": ["abc123"],
  "tags": [
    "#c": ["concept-graph-testnet-901"],
    "#s": ["wordType_word"],
  ]
}
```

## References

- `word` is introduced in [DIP-100](../100.md).
- glossary entry: [word](../../../glossary/word.md), [word type](../../../glossary/wordType.md)
