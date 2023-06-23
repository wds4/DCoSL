```json
{
  "wordData": {
    "slug": "relationship",
    "version": "hybridSandbox",
    "wordTypes": ["wordType", "jsonSchema"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "relationship",
          "version": "hybridSandbox"
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
    "propertyPath": "relationshipData",
    "description": "A edge bewtween two nodes in a graph, as specified according to the DCoSL protocol."
  },
  "jsonSchemaData": {
    "name": "relationship",
    "title": "Relationship",
    "$schema": "http://json-schema.org/draft-07/schema",
    "type": "object",
    "required": [
      "relationshipData"
    ],
    "definitions": {
      "nostrWord": {
        "type": "object",
        "description": "enough information to identify a word uniquely. The slug is enough in some cases and is required. Name and title may be useful for UX purposes but is not required. The nostr event id and other fields may be needed in some cases if the slug alone produces any ambiguity.",
        "required": [
          "slug"
        ],
        "properties": {
          "slug": {
            "type": "string"
          },
          "name": {
            "type": "string"
          },
          "title": {
            "type": "string"
          },
          "id": {
            "description:": "the nostr event id corresponding to the word in question",
            "type": "string"
          },
          "stewardPubkey": {
            "type": "string"
          },
          "version": {
            "type": "string"
          }
        }
      },
      "nostrRelationshipType": {
        "type": "object",
        "description": "enough information to identify the relationship type uniquely. The slug is enough in some cases and is required. Name and title may be useful for UX purposes but is not required. The nostr event id and other fields may be needed in some cases if the slug alone produces any ambiguity.",
        "required": [
          "slug"
        ],
        "properties": {
          "slug": {
            "type": "string",
            "description": "the slug of the relationshipType; e.g., isASubcategoryOf"
          },
          "name": {
            "type": "string",
            "description": "the name of the relationshipType; e.g., is a subcategory of"
          },
          "title": {
            "type": "string",
            "description": "the title of the relationshipType; e.g., Is a Subcategory Of"
          },
          "id": {
            "description:": "the nostr event id corresponding to the word in question",
            "type": "string"
          },
          "stewardPubkey": {
            "type": "string"
          },
          "version": {
            "type": "string"
          }
        }
      }
    },
    "properties": {
      "relationshipData": {
        "type": "object",
        "name": "relationship data",
        "title": "Nostr Curated List Data",
        "description": "data about this nostrCuratedList",
        "required": [
          "nodeFrom",
          "relationshipType",
          "nodeTo"
        ],
        "definitions": {},
        "properties": {
          "nodeFrom": {
            "$ref": "#/definitions/nostrWord"
          },
          "relationshipType": {
            "$ref": "#/definitions/nostrRelationshipType"
          },
          "nodeTo": {
            "$ref": "#/definitions/nostrWord"
          }
        }
      }
    }
  }
}
```

An example item on this list:

```json
{
  "relationshipData": {
    "nodeFrom": {
      "slug": "categoryOf_iPhones"
    },
    "relationshipType": {
      "slug": "isASubcategoryOf"
    },
    "nodeTo": {
      "slug": "categoryOf_smartphones"
    }
  }
}
```

NOTE: the above word type (above) may not match the published version (below) due to editing subsequent to publishing.

This example ought to validate against the JSON file. To test this out, go to [this site](https://www.jsonschemavalidator.net) and paste the JSON file (below) to the field on the left and the relationship word (above) to the field on the right.

The JSON Schema extracted from the above word (the word with `wordData.slug` = `relationship`) is this:

```json
{
  "name": "relationship",
  "title": "Relationship",
  "$schema": "http://json-schema.org/draft-07/schema",
  "type": "object",
  "required": [
    "relationshipData"
  ],
  "definitions": {
    "nostrWord": {
      "type": "object",
      "description": "enough information to identify a word uniquely. The slug is enough in some cases and is required. Name and title may be useful for UX purposes but is not required. The nostr event id and other fields may be needed in some cases if the slug alone produces any ambiguity.",
      "required": [
        "slug"
      ],
      "properties": {
        "slug": {
          "type": "string"
        },
        "name": {
          "type": "string"
        },
        "title": {
          "type": "string"
        },
        "id": {
          "description:": "the nostr event id corresponding to the word in question",
          "type": "string"
        },
        "stewardPubkey": {
          "type": "string"
        },
        "version": {
          "type": "string"
        }
      }
    },
    "nostrRelationshipType": {
      "type": "object",
      "description": "enough information to identify the relationship type uniquely. The slug is enough in some cases and is required. Name and title may be useful for UX purposes but is not required. The nostr event id and other fields may be needed in some cases if the slug alone produces any ambiguity.",
      "required": [
        "slug"
      ],
      "properties": {
        "slug": {
          "type": "string",
          "description": "the slug of the relationshipType; e.g., isASubcategoryOf"
        },
        "name": {
          "type": "string",
          "description": "the name of the relationshipType; e.g., is a subcategory of"
        },
        "title": {
          "type": "string",
          "description": "the title of the relationshipType; e.g., Is a Subcategory Of"
        },
        "id": {
          "description:": "the nostr event id corresponding to the word in question",
          "type": "string"
        },
        "stewardPubkey": {
          "type": "string"
        },
        "version": {
          "type": "string"
        }
      }
    }
  },
  "properties": {
    "relationshipData": {
      "type": "object",
      "name": "relationship data",
      "title": "Nostr Curated List Data",
      "description": "data about this nostrCuratedList",
      "required": [
        "nodeFrom",
        "relationshipType",
        "nodeTo"
      ],
      "definitions": {},
      "properties": {
        "nodeFrom": {
          "$ref": "#/definitions/nostrWord"
        },
        "relationshipType": {
          "$ref": "#/definitions/nostrRelationshipType"
        },
        "nodeTo": {
          "$ref": "#/definitions/nostrWord"
        }
      }
    }
  }
}
```

The above word (the word with `wordData.slug` = `relationship` at the top of the page) was published to nostr using the following event:

```json
{
    "content": "{\"wordData\":{\"slug\":\"relationship\",\"version\":\"hybridSandbox\",\"wordTypes\":[\"wordType\",\"jsonSchema\"],\"metaData\":{\"nostr\":{\"stewardPubkey\":\"c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa\",\"uniqueIDs\":{\"slug\":\"relationship\",\"version\":\"hybridSandbox\"}}}},\"wordTypeData\":{\"oSlug\":{\"singular\":\"relationship\",\"plural\":\"relationships\"},\"oName\":{\"singular\":\"relationship\",\"plural\":\"relationships\"},\"oTitle\":{\"singular\":\"Relationship\",\"plural\":\"Relationships\"},\"description\":\"A edge bewtween two nodes in a graph, as specified according to the DCoSL protocol.\"},\"jsonSchemaData\":{\"name\":\"relationship\",\"title\":\"Relationship\",\"$schema\":\"http://json-schema.org/draft-07/schema\",\"type\":\"object\",\"required\":[\"relationshipData\"],\"definitions\":{\"nostrWord\":{\"type\":\"object\",\"description\":\"enough information to identify a word uniquely. The slug is enough in some cases and is required. Name and title may be useful for UX purposes but is not required. The nostr event id and other fields may be needed in some cases if the slug alone produces any ambiguity.\",\"required\":[\"slug\"],\"properties\":{\"slug\":{\"type\":\"string\"},\"name\":{\"type\":\"string\"},\"title\":{\"type\":\"string\"},\"id\":{\"description:\":\"the nostr event id corresponding to the word in question\",\"type\":\"string\"},\"stewardPubkey\":{\"type\":\"string\"},\"version\":{\"type\":\"string\"}}},\"nostrRelationshipType\":{\"type\":\"object\",\"description\":\"enough information to identify the relationship type uniquely. The slug is enough in some cases and is required. Name and title may be useful for UX purposes but is not required. The nostr event id and other fields may be needed in some cases if the slug alone produces any ambiguity.\",\"required\":[\"slug\"],\"properties\":{\"slug\":{\"type\":\"string\",\"description\":\"the slug of the relationshipType; e.g., isASubcategoryOf\"},\"name\":{\"type\":\"string\",\"description\":\"the name of the relationshipType; e.g., is a subcategory of\"},\"title\":{\"type\":\"string\",\"description\":\"the title of the relationshipType; e.g., Is a Subcategory Of\"},\"id\":{\"description:\":\"the nostr event id corresponding to the word in question\",\"type\":\"string\"},\"stewardPubkey\":{\"type\":\"string\"},\"version\":{\"type\":\"string\"}}}},\"properties\":{\"relationshipData\":{\"type\":\"object\",\"name\":\"relationship data\",\"title\":\"Nostr Curated List Data\",\"description\":\"data about this nostrCuratedList\",\"required\":[\"nodeFrom\",\"relationshipType\",\"nodeTo\"],\"definitions\":{},\"properties\":{\"nodeFrom\":{\"$ref\":\"#/definitions/nostrWord\"},\"relationshipType\":{\"$ref\":\"#/definitions/nostrRelationshipType\"},\"nodeTo\":{\"$ref\":\"#/definitions/nostrWord\"}}}}}}",
    "kind": 9902,
    "tags": [
        [
            "c",
            "concept-graph-testnet-2"
        ],
        [
            "t",
            "createWord"
        ],
        [
            "s",
            "word"
        ],
        [
            "w",
            "relationship"
        ]
    ],
    "created_at": 1687054844,
    "pubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
    "id": "6a7794b2b1d1cb33c05473fe2a52f4460eec63311e851e3c3fa8e787ca7d88fb",
    "sig": "5b1e828db3c81029c6dc51b61a296c5bcd0faaf2a0da847ca80c87f96c12fe3facc1eed72f7e7e3730de2a5062972b6b0f7ee80423fea9b3b0bf18963252cc44"
}
```

It can be retrieved using one of the following filters:

```json
{
  "since": 0,
  "kinds": [9902],
  "authors": ["c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa"],
  "#c": ["concept-graph-testnet-902"],
  "#w": ["relationship"],
}
```

```json
{
  "ids": ["6a7794b2b1d1cb33c05473fe2a52f4460eec63311e851e3c3fa8e787ca7d88fb"]
}
```
