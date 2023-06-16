```json
{
    "wordData": {
        "slug": "jsonSchemaFor_graph",
        "name": "json schema for graph",
        "title": "JSON Schema for Graph",
        "metaData": {
            "nostr": {
                "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"
                "uniqueIDs": {
                     "slug": "jsonSchemaFor_graph"
                 }
            }
        }
    },
    "jsonSchemaData": {
        "name": "widget",
        "title": "Widget",
        "type": "object",
        "required": [
            "widgetData",
            version: 1
        ],
        "definitions": {},
        "properties": {
            "widgetData": {
                "type": "object",
                "name": "widget data",
                "title": "Widget Data",
                "description": "data about this widget",
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
