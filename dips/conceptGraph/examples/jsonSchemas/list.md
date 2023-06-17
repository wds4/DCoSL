```json
{
    "wordData": {
        "slug": "jsonSchemaFor_list",
        "name": "json schema for list",
        "title": "JSON Schema for List",
        "metaData": {
            "nostr": {
                "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"
                "uniqueIDs": {
                     "slug": "jsonSchemaFor_list"
                 }
            }
        }
    },
    "jsonSchemaData": {
        "name": "list",
        "title": "List",
        "$schema": "http://json-schema.org/draft-07/schema",
        "type": "object",
        "required": [
            "listData"
        ],
        "definitions": {},
        "properties": {
            "listData": {
                "type": "object",
                "name": "list data",
                "title": "List Data",
                "description": "data about this list",
                "require": true,
                "required": [
                    "name",
                    "description"
                ],
                "definitions": {},
                "properties": {
                    "name": {
                        "type": "object",
                        "required": [
                            "singular",
                            "plural"
                        ],
                        "properties": {
                            "singular": {
                                "type": "string"
                            },
                            "plural": {
                                "type": "string"
                            }
                        }
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
