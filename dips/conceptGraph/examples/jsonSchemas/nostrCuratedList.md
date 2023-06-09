```json
{
    "wordData": {
        "slug": "jsonSchemaFor_nostrCuratedList",
        "name": "json schema for nostr curated list",
        "title": "JSON Schema for Nostr Curated List",
        "metaData": {
            "nostr": {
                "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"
                "uniqueIDs": {
                     "slug": "jsonSchemaFor_nostrCuratedList"
                 }
            }
        }
    },
    "jsonSchemaData": {
        "name": "nostrCuratedList",
        "title": "NostrCuratedList",
        "$schema": "http://json-schema.org/draft-07/schema",
        "type": "object",
        "required": [
            "nostrCuratedListData"
        ],
        "definitions": {},
        "properties": {
            "nostrCuratedListData": {
                "type": "object",
                "name": "nostr curated list data",
                "title": "Nostr Curated List Data",
                "description": "data about this nostrCuratedList",
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
