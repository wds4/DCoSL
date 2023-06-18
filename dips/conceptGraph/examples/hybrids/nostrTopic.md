```json
{
    "wordData": {
        "slug": "nostrTopic",
        "name": "nostr topic",
        "title": "Nostr Topic",
        "version": "testnet-902",
        "wordTypes": ["wordType","jsonSchema"],
        "metaData": {
            "nostr": {
                "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
                "uniqueIDs": {
                    "slug": "nostrTopic",
                    "version": "testnet-902"
                }
            }
        }
    },
    "wordTypeData": {
        "oName": {
            "singular": "nostr topic",
            "plural": "nostr topics"
        },
        "oTitle": {
            "singular": "Nostr Topic",
            "plural": "Nostr Topics"
        },
        "oSlug": {
            "singular": "nostrTopic",
            "plural": "nostrTopics"
        },
        "description": "a list of topics for use in organizing and curating your nostr feed",
        "propertyPath": "nostrTopicData"
    },
    "jsonSchemaData": {
        "description": "This is the JSON Schema used to create and validate object files for the representation of instances of the list of nostr topics",
        "name": "json schema for an item on the list of nostr topics",
        "title": "JSON Schema for an Item on the List of Nostr Topics",
        "$schema": "http://json-schema.org/draft-07/schema",
        "type": "object",
        "required": [
            "nostrTopicData"
        ],
        "definitions": {},
        "properties": {
            "nostrTopicData": {
                "type": "object",
                "name": "nostr topic data",
                "title": "Nostr Topic Data",
                "description": "data about this nostr topic",
                "required": [
                    "name"
                ],
                "definitions": {},
                "properties": {
                    "name": {
                        "type": "string"
                    },
                    "title": {
                        "type": "string"
                    },
                    "slug": {
                        "type": "string"
                    },
                    "description": {
                        "type": "string"
                    }
                }
            }
        }
    }
}
```

This was published to nostr using this event:

```json
{
    "content": "{\"wordData\":{\"slug\":\"nostrTopic\",\"name\":\"nostr topic\",\"title\":\"Nostr Topic\",\"version\":\"testnet-902\",\"wordTypes\":[\"wordType\",\"jsonSchema\"],\"metaData\":{\"nostr\":{\"stewardPubkey\":\"c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa\",\"uniqueIDs\":{\"slug\":\"nostrTopic\",\"version\":\"testnet-902\"}}}},\"wordTypeData\":{\"oName\":{\"singular\":\"nostr topic\",\"plural\":\"nostr topics\"},\"oTitle\":{\"singular\":\"Nostr Topic\",\"plural\":\"Nostr Topics\"},\"oSlug\":{\"singular\":\"nostrTopic\",\"plural\":\"nostrTopics\"},\"description\":\"a list of topics for use in organizing and curating your nostr feed\",\"propertyPath\":\"nostrTopicData\"},\"jsonSchemaData\":{\"description\":\"This is the JSON Schema used to create and validate object files for the representation of instances of the list of nostr topics\",\"name\":\"json schema for an item on the list of nostr topics\",\"title\":\"JSON Schema for an Item on the List of Nostr Topics\",\"type\":\"object\",\"required\":[\"nostrTopicData\"],\"definitions\":{},\"properties\":{\"nostrTopicData\":{\"type\":\"object\",\"name\":\"nostr topic data\",\"title\":\"Nostr Topic Data\",\"description\":\"data about this nostr topic\",\"required\":[\"name\"],\"definitions\":{},\"properties\":{\"name\":{\"type\":\"string\"},\"title\":{\"type\":\"string\"},\"slug\":{\"type\":\"string\"},\"description\":{\"type\":\"string\"}}}}}}",
    "kind": 9902,
    "tags": [
        [
            "c",
            "concept-graph-testnet-902"
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
            "nostrTopic"
        ]
    ],
    "created_at": 1687122463,
    "pubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
    "id": "ce37e3fe2a2d55cb1200e3c2bb25226e5518e8d28e60c2e927f9bdeed1de5662",
    "sig": "b475de57d97eba9ea629fdc3058f6cafd0d7f6a52b8b35a498ea9549baf473a9588b75a074e92222c6da7a5e61aab469e59ec922328a79a658bcbc5f32751e84"
}
```

It can be retrieved using either of the filters below:

```json
{
  "since": 0,
  "kinds": [9902],
  "authors": ["c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"],
  "#c": ["concept-graph-testnet-902"],
  "#w": ["nostrTopic"],
}
```

```json
{
    "ids": ["ce37e3fe2a2d55cb1200e3c2bb25226e5518e8d28e60c2e927f9bdeed1de5662"]
}
```

