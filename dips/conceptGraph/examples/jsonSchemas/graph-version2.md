See [this file](https://github.com/wds4/DCoSL/blob/main/dips/conceptGraph/examples/graphs/graph-version2-example.md) for an example of a graph that follows the below format.

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
                        "require": true,
                        "items": {
                            "type": "string"
                        }
                    },
                    "relationships": {
                        "type": "array",
                        "require": true,
                        "prefixItems": [
                            { "type": "string" },
                            { "type": "string" },
                            { "type": "string" }
                        ],
                        "items": false
                    }
                }
            }
        }
    }
}
```
