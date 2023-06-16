
```json
{
    "wordData": {
        "slug": "jsonSchemaFor_widget",
        "name": "json schema for widget",
        "title": "JSON Schema for Widget",
        "metaData": {
            "nostr": {
                "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"
                "uniqueIDs": {
                     "slug": "jsonSchemaFor_widget"
                 }
            }
        }
    },
    "jsonSchemaData": {
        "name": "widget",
        "title": "Widget",
        "type": "object",
        "required": [
            "widgetData"
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
