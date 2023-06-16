# Declaration of `word`

## Declaration

as per [DIP-102](../102.md)

```json
{
  "wordData": {
    "slug": "wordType_word",
    "name": "word type: word",
    "title": "Word Type: Word",
    "wordTypes": ["wordType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
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
    "description": "A node in a graph, formatted in json, with additional requirements and conventions specified according to the DCoSL protocol."
  }
}
```

## Publication to nostr

as per [DIP-101](../101.md)

```json
{
    "content": "{\n  \"wordData\": {\n    \"slug\": \"wordType_word\",\n    \"name\": \"word type: word\",\n    \"title\": \"Word Type: Word\",\n    \"wordTypes\": [\"wordType\"],\n    \"metaData\": {\n      \"nostr\": {\n        \"stewardPubkey\": \"c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa\",\n        \"uniqueIDs\": {\n          \"slug\": \"wordType_word\"\n        }\n      }\n    }\n  },\n  \"wordTypeData\": {\n    \"slug\": \"word\",\n    \"name\": \"word\",\n    \"title\": \"word\",\n    \"description\": \"A node in a graph, formatted in json, with additional requirements specified in DIP-100\"\n  }\n}",
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
            "wordType_word"
        ]
    ],
    "created_at": 1686863585,
    "pubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
    "id": "2a856f2db29f1215462808d7a57a3b53ea2989c65ba0f387526c679c28ca13fb",
    "sig": "769b741c17cad860ac211b17bbd3a3ee970e67387dc11a26b8eec994a75fca377a38a1c3801ad738507921f60993fd8e1771fe44076d4601e606fa60b0d17251"
}
```

(NOTE: hypothetical example only; note with id 2a856f2db29f1215462808d7a57a3b53ea2989c65ba0f387526c679c28ca13fb has not actually been published!)

As per DIP 101 (updated for testnet-2), all versions of the above word can be found in nostr (testnet-2) using the following filter:

```json
{
  "since": 0,
  "kinds": [9902],
  "authors": ["c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"],
  "tags": [
    ["c", "concept-graph-testnet-902"],
    ["w", "wordType_word"]
  ]
}
```

## References

- `word` is introduced in [DIP-100](../100.md).
- glossary entry: [word](../../../glossary/word.md), [word type](../../../glossary/wordType.md)
