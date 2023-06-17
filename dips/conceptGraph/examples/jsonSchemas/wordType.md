```json
{
    "wordData": {
        "slug": "jsonSchemaFor_wordType",
        "name": "json schema for word type",
        "title": "JSON Schema for Word Type",
        "metaData": {
            "nostr": {
                "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"
                "uniqueIDs": {
                     "slug": "jsonSchemaFor_wordType"
                 }
            }
        }
    },
    "jsonSchemaData": {
        "name": "word type",
        "title": "Word Type",
        "$schema": "http://json-schema.org/draft-07/schema",
        "type": "object",
        "required": [
            "wordTypeData"
        ],
        "definitions": {},
        "properties": {
            "wordTypeData": {
                "type": "object",
                "name": "word type data",
                "title": "Word Type Data",
                "description": "data about this word type",
                "require": true,
                "required": [
                    "name",
                    "title",
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
                    "title": {
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
