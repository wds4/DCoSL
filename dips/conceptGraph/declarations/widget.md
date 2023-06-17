Declaration of `widget`
=====

## Declaration

as per [DIP-102](../102.md)

```json
{
  "wordData": {
    "slug": "widget",
    "wordTypes": ["wordType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "widget"
        }
      }
    }
  },
  "wordTypeData": {
    "slug": "widget",
    "oName": {
      "singular": "widget",
      "plural": "widgets"
    },
    "oTitle": {
      "singular": "Widget",
      "plural": "Widgets"
    },
    "description": "lorem ipsum"
  }
}
```

NOTE: the above word type (above) may not match the published version (below) due to editing subsequent to publishing.

## Publication to nostr

as per [DIP-901](../../networking/nostr/901.md)

```json
{
    "content": "{\"wordData\":{\"slug\":\"widget\",\"wordTypes\":[\"wordType\"],\"metaData\":{\"nostr\":{\"stewardPubkey\":\"c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa\",\"uniqueIDs\":{\"slug\":\"widget\"}}}},\"wordTypeData\":{\"slug\":\"widget\",\"oName\":{\"singular\":\"widget\",\"plural\":\"widgets\"},\"oTitle\":{\"singular\":\"Widget\",\"plural\":\"Widgets\"},\"description\":\"lorem ipsum\"}}",
    "kind": 9902,
    "tags": [
        [
            "c",
            "concept-graph-testnet-2"
        ],
        [
            "t",
            "createWord"
        ],
        [
            "s",
            "word"
        ],
        [
            "w",
            "widget"
        ]
    ],
    "created_at": 1686976069,
    "pubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
    "id": "68209b0796f27e08c6c252ac8054441dd1e470a2f405ebaabbd343e85712039b",
    "sig": "584a7576e658311022e1ba061d99a37a3bb63208ae483a5811b01ec9cdad42c44faa2853ccd9010cede09ca5876210d3d60bf2b53a190b46377451f18737865a"
}
```

## Retrieval from nostr

As per DIP 101 (updated for testnet-2), all versions of the above word can be found in nostr (testnet-2) using the following filter:

```json
{
  "since": 0,
  "kinds": [9902],
  "authors": ["c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"],
  "#c": ["concept-graph-testnet-902"],
  "#w": ["word"],
}
```

or

```json
{
  "ids": ["68209b0796f27e08c6c252ac8054441dd1e470a2f405ebaabbd343e85712039b"],
}
```

## References

- relevant glossary entry: [word type](../../../glossary/wordType.md)
