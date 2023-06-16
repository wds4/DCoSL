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
                     "slug": "jsonSchemaFor_graph",
                     "version": 1
                 }
            }
        }
    },
    "jsonSchemaData": {
        "name": "graph",
        "title": "Graph",
        "type": "object",
        "required": [
            "graphData",
        ],
        "definitions": {},
        "properties": {
            "graphData": {
                "type": "object",
                "name": "widget data",
                "title": "Widget Data",
                "description": "data about this graph",
                "require": true,
                "required": [
                    "name"
                ],
                "definitions": {},
                "properties": {
                    "slug": {
                        "type": "string",
                        "require": false
                    },
                    "nodes": {
                        "type": "array",
                        "require": true
                    },
                    "relationships": {
                        "type": "array",
                        "require": true
                    },
                    "relationshipTypes": {
                        "type": "array",
                        "require": true
                    },
                    "importedGraphs": {
                        "type": "array",
                        "require": true
                    }
                }
            }
        }
    }
}
```
