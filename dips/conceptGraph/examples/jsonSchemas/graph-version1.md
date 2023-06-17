See [this file](https://github.com/wds4/DCoSL/blob/main/dips/conceptGraph/examples/graphs/graph-version1-example.md) for an example of a graph that follows the below format.

```json
{
    "wordData": {
        "slug": "jsonSchemaFor_graph",
        "version": "compact",
        "name": "json schema for graph",
        "title": "JSON Schema for Graph",
        "metaData": {
            "nostr": {
                "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"
                "uniqueIDs": {
                     "slug": "jsonSchemaFor_graph",
                     "version": "compact"
                 }
            }
        }
    },
    "jsonSchemaData": {
        "name": "graph",
        "title": "Graph",
        "$schema": "http://json-schema.org/draft-07/schema",
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
                    "nodes",
                    "relationships"
                ],
                "definitions": {},
                "properties": {
                    "slug": {
                        "type": "string"
                    },
                    "nodes": {
                        "type": "array",
                        "items": {
                            "type": "string"
                        }
                    },
                    "relationships": {
                        "type": "array",
                        "items": {
                            "type": "array",
                            "minItems": 3,
                            "maxItems": 3,
                            "items": {
                                "type": "string"
                            }
                        }
                    }
                }
            }
        }
    }
}
```
