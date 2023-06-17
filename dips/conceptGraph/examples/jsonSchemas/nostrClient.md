```json
{
    "wordData": {
        "slug": "jsonSchemaFor_nostrClients",
        "metaData": {
            "nostr": {
                "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"
                "uniqueIDs": {
                     "slug": "jsonSchemaFor_nostrClients"
                 }
            }
        }
    },
    "jsonSchemaData": {
        "description": "This is the JSON Schema used to create and validate object files for the representation of instances of the list of nostr clients",
        "name": "json schema for an instance of nostr client",
        "title": "JSON Schema for an Instance of Nostr Client",
        "$schema": "http://json-schema.org/draft-07/schema",
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
