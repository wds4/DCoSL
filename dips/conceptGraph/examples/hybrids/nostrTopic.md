```json
{
    "wordData": {
        "slug": "nostrTopic",
        "name": "nostr topic",
        "title": "Nostr Topic",
        "version": "testnet-2",
        "wordTypes": ["wordType","jsonSchema"],
        "metaData": {
            "nostr": {
                "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
                "uniqueIDs": {
                    "slug": "nostrTopic",
                    "version": "testnet-2"
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
    "content": "{\"wordData\":{\"slug\":\"nostrTopic\",\"name\":\"nostr topic\",\"title\":\"Nostr Topic\",\"version\":\"testnet-2\",\"wordTypes\":[\"wordType\",\"jsonSchema\"],\"metaData\":{\"nostr\":{\"stewardPubkey\":\"c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa\",\"uniqueIDs\":{\"slug\":\"nostrTopic\",\"version\":\"testnet-2\"}}}},\"wordTypeData\":{\"oName\":{\"singular\":\"nostr topic\",\"plural\":\"nostr topics\"},\"oTitle\":{\"singular\":\"Nostr Topic\",\"plural\":\"Nostr Topics\"},\"oSlug\":{\"singular\":\"nostrTopic\",\"plural\":\"nostrTopics\"},\"description\":\"a list of topics for use in organizing and curating your nostr feed\",\"propertyPath\":\"nostrTopicData\"},\"jsonSchemaData\":{\"description\":\"This is the JSON Schema used to create and validate object files for the representation of instances of the list of nostr topics\",\"name\":\"json schema for an item on the list of nostr topics\",\"title\":\"JSON Schema for an Item on the List of Nostr Topics\",\"type\":\"object\",\"required\":[\"nostrTopicData\"],\"definitions\":{},\"properties\":{\"nostrTopicData\":{\"type\":\"object\",\"name\":\"nostr topic data\",\"title\":\"Nostr Topic Data\",\"description\":\"data about this nostr topic\",\"required\":[\"name\"],\"definitions\":{},\"properties\":{\"name\":{\"type\":\"string\"},\"title\":{\"type\":\"string\"},\"slug\":{\"type\":\"string\"},\"description\":{\"type\":\"string\"}}}}}}",
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
            "nostrTopic"
        ]
    ],
    "created_at": 1687122069,
    "pubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
    "id": "1adc159b97507552511735f55c664668e9a74c55cfa0f2e64f370c5d4462b45b",
    "sig": "74d456c6c9c71ed5f84b5f768bcf31da099e1a0d297933d89f77c4ed43a2836e11ed4fd67ce54c2dcd4ca779b1de15e2d2d15d096e19e33ae0048c6144ed2736"
}
```

It can be retrieved using either of the filters below:

```json
```

```json
```

