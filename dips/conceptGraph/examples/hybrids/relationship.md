```json
{
  "wordData": {
    "slug": "relationship",
    "wordTypes": ["wordType", "jsonSchema"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "relationship"
        }
      }
    }
  },
  "wordTypeData": {
    "oSlug": {
      "singular": "relationship",
      "plural": "relationships"
    },
    "oName": {
      "singular": "relationship",
      "plural": "relationships"
    },
    "oTitle": {
      "singular": "Relationship",
      "plural": "Relationships"
    },
    "description": "A edge bwtween two nodes in a graph, as specified according to the DCoSL protocol."
  },
  "jsonSchemaData": {
    "name": "relationship",
    "title": "Relationship",
    "$schema": "http://json-schema.org/draft-07/schema",
    "type": "object",
    "required": [
      "relationshipData"
    ],
    "definitions": {},
    "properties": {
      "relationshipData": {
        "type": "object",
        "name": "relationship data",
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
