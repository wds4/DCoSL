# Declaration of `troll` (version 2)

## Declaration

```json
{
  "wordData": {
    "slug": "troll",
    "version": "more sophisticated description",
    "wordTypes": ["wordType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "troll",
          "version": "more sophisticated description"
        }
      }
    }
  },
  "wordTypeData": {
    "slug": "troll",
    "name": "troll",
    "title": "Troll",
    "description": "A troll is a user who angers and thereby engagges with other users by making intentionally inflamamtory or incorrect statements. In some cases, the underlying motivation of so-called 'trolling' is to elicit the truth on some topic of interest by triggering those who know it to provide a clear and in depth explanation. Unfortunately, the mindset of the troll is to be intentionally dense. As such, the troll frequently renders himself incapable of accepting the truth even when it smacks him on the head."
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
  "#v": ["more sophisticated description"],
  "#w": ["troll"],
}
```

or

```json
{
  "ids": [""],
}
```

## References

- `concept` is introduced in [DIP-111](../111.md).
- relevant glossary entry: [word type](../../../glossary/wordType.md)
