```json
{
    "wordData": {
        "slug": "jsonSchemaFor_graph",
        "version": 2,
        "name": "json schema for graph",
        "title": "JSON Schema for Graph",
        "metaData": {
            "nostr": {
                "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"
                "uniqueIDs": {
                     "slug": "jsonSchemaFor_graph",
                     "version": 2
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
        "definitions": {
            "nostrWordData": {
                "type": "object",
                "required": false,
                "properties": {
                    "eventID": {
                        "type": "string"
                    },
                    "stewardPubkey": {
                        "type": "string"
                    },
                    "slug": {
                        "type": "string"
                    }                                    
                }
            },
            "ipfsWordData": {
                "type": "object",
                "required": false,
                "properties": {
                    "ipfs": {
                        "type": "string"
                    },
                    "ipns": {
                        "type": "string"
                    },
                    "slug": {
                        "type": "string"
                    }                                    
                }
            }
        },
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
                        "require": true,
                        "items": {
                            "type": "object",
                            "properties": {
                                "slug": {
                                    "type": "string",
                                    "required": true
                                },
                                "nostr": {
                                    "$ref": "#/definitions/nostrWordData",
                                    "required": false
                                },
                                "ipfs": {
                                    "$ref": "#/definitions/ipfsWordData",
                                    "required": false
                                }
                            }
                        }
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
