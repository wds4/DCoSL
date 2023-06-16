nostr clients
=====



```json
{
    "nostrCuratedListData": {
        "name": {
            "singular": "nostr client",
            "plural": "nostr clients"
        },
        "title": {
            "singular": "Nostr Client",
            "plural": "Nostr Clients"
        },
        "slug": {
            "singular": "nostrClient",
            "plural": "nostrClients"
        },
        "description": "a list of all nostr clients",
        "propertyPath": "nostrClientData"
    },
    "jsonSchemaData": {
        "description": "This is the JSON Schema used to create and validate object files for the representation of instances of the list of nostr clients",
        "name": "json schema for an instance of nostr client",
        "title": "JSON Schema for an Instance of Nostr Client",
        "type": "object",
        "required": [
            "nostrClientData"
        ],
        "definitions": {},
        "properties": {
            "nostrClientData": {
                "type": "object",
                "name": "nostr client data",
                "title": "Nostr Client Data",
                "description": "data about this nostr client",
                "require": true,
                "required": [
                    "name"
                ],
                "definitions": {},
                "properties": {
                    "name": {
                        "type": "string",
                        "require": true
                    },
                    "title": {
                        "type": "string",
                        "require": false
                    },
                    "slug": {
                        "type": "string",
                        "require": false
                    },
                    "description": {
                        "type": "string",
                        "require": false
                    }
                }
            }
        }
    }
}
```

Note that the above example:
- wordData has been omitted. If it had been included, it would have included the following information:

```json
{
  "wordData": {
    "slug": "nostrCuratedList_nostrClients",
    "wordTypes": ["nostrCuratedList", "jsonSchema"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "nostrCuratedList_nostrClients"
        }
      }
    }
  }
}
```

- jsonSchema has been included in the same word. This is nonstandard. Normally the json schema would be a separate word.


It was published using this event:

```json
{
    "id": "7e92c80fb7d3fa7bec453c8b3c6db306bdde50f7eee34e76a880fe0ab770d485",
    "pubkey": "e5272de914bd301755c439b88e6959a43c9d2664831f093c51e9c799a16a102f",
    "created_at": 1679105853,
    "kind": 9901,
    "tags": [
        [
            "c",
            "concept-graph-testnet-901"
        ],
        [
            "t",
            "createInstance"
        ],
        [
            "s",
            "nostrCuratedList"
        ]
    ],
    "content": "{\"nostrCuratedListData\":{\"name\":{\"singular\":\"nostr client\",\"plural\":\"nostr clients\"},\"title\":{\"singular\":\"Nostr Client\",\"plural\":\"Nostr Clients\"},\"slug\":{\"singular\":\"nostrClient\",\"plural\":\"nostrClients\"},\"description\":\"a list of all nostr clients\",\"propertyPath\":\"nostrClientData\"},\"jsonSchemaData\":{\"description\":\"This is the JSON Schema used to create and validate object files for the representation of instances of the list of nostr clients\",\"name\":\"json schema for an instance of nostr client\",\"title\":\"JSON Schema for an Instance of Nostr Client\",\"type\":\"object\",\"required\":[\"nostrClientData\"],\"definitions\":{},\"properties\":{\"nostrClientData\":{\"type\":\"object\",\"name\":\"nostr client data\",\"title\":\"Nostr Client Data\",\"description\":\"data about this nostr client\",\"require\":true,\"required\":[\"name\"],\"definitions\":{},\"properties\":{\"name\":{\"type\":\"string\",\"require\":true},\"title\":{\"type\":\"string\",\"require\":false},\"slug\":{\"type\":\"string\",\"require\":false},\"description\":{\"type\":\"string\",\"require\":false}}}}}}",
    "sig": "4a67bdb8d514a200ee6c1ca7f5f7437126a957175016be3091ec9fe5ce8ab90e6b615cf60a100ed61ba6f15e516d51802e047bb5c241c95fc5e892cf27fbe551"
}
```

