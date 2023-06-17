# Declaration of `troll` (version 1)

## Declaration

Note that the declaration below contains the `wordData.version` property, indicating the intention of the publisher (the stewardPubkey) to publish multiple versions.

Note also that the `wordData.metaData` property is absent. However, it is present in the example at the bottom of this page, indicating the source of the download.

```json
{
  "wordData": {
    "slug": "troll",
    "version": "simplistic description",
    "wordTypes": ["wordType"]
  },
  "wordTypeData": {
    "oSlug": {
      "singular": "troll",
      "plural": "trolls"
    },
    "oName": {
      "singular": "troll",
      "plural": "trolls"
    },
    "oTitle": {
      "singular": "Troll",
      "plural": "Trolls"
    },
    "description": "A troll is a user who is just super duper mean to everyone, all the time."
  }
}
```

NOTE: the above word type (above) may not match the published version (below) due to editing subsequent to publishing.

## Publication to nostr

as per [DIP-901](../../networking/nostr/901.md)

```json
{
    "content": "{\"wordData\":{\"slug\":\"troll\",\"version\":\"simplistic description\",\"wordTypes\":[\"wordType\"]},\"wordTypeData\":{\"slug\":\"troll\",\"name\":\"troll\",\"title\":\"Troll\",\"description\":\"A troll is a user who is just super duper mean to everyone, all the time.\"}}",
    "created_at": 1686965288,
    "id": "8819032ed7682c316cb7e13a0f8878d144c0f20cc8fef1e9804a66a4576a9dbc",
    "kind": 9902,
    "pubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
    "sig": "c8c9afc78c9ac9e2cfb7599b6a957c97fb1d8ed386151e7013534cf761513c447e850021472071c843d8e2e741704664bda175649186f95dfe85b44185659882",
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
            "troll"
        ]
    ]
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
  "#v": ["simplisticDescription"],
  "#w": ["troll"],
}
```

or

```json
{
  "ids": ["8819032ed7682c316cb7e13a0f8878d144c0f20cc8fef1e9804a66a4576a9dbc"],
}
```

The local copy of the word, after retrieval from the network and local editing, may look like this:

```json
{
  "wordData": {
    "slug": "antagonizer_6a9dbc",
    "name": "antagonizer",
    "title": "Antagonizer",
    "wordTypes": ["wordType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "troll",
          "version": "simplistic description",
          "id": "8819032ed7682c316cb7e13a0f8878d144c0f20cc8fef1e9804a66a4576a9dbc",
          "edits": false
        }
      }
    }
  },
  "wordTypeData": {
    "slug": "troll",
    "name": "troll",
    "title": "Troll",
    "description": "A troll is a user who is just super duper mean to everyone, all the time."
  }
}
```

Note that the local copy:
- The `wordData.slug` property has been changed.
- `wordData.name` and `wordData.title` fields have been added.
- The `wordData.version` property has been removed.
- The `edits` property is set to false, and no edits have been made to the word outside of the `wordData` top-level property. The edits property indicates whether any changes have been made locally to the word after download from the original author. 

## References

- `concept` is introduced in [DIP-111](../111.md).
- relevant glossary entry: [word type](../../../glossary/wordType.md)
