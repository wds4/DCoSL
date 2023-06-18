This is a combination `wordTYpe` and `jsonSchema`. As a `wordType`, tecnically the issuance of this word is a `declaration`.

Basically I've taken the word type and the json schema for nostrCuratedList, put them together into one word, changed the name (especially the slug, so I don't confuse it with the original nostrCuratedList) and added a version. I then made alterations to `jsonSchemaData`, which is what makes it a complex list.


```json
{
  "wordData": {
    "slug": "nostrComplexList",
    "wordTypes": ["wordType","jsonSchema"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "nostrComplexList"
        }
      }
    }
  },
  "wordTypeData": {
    "oSlug": {
      "singular": "nostrComplexList",
      "plural": "nostrComplexLists"
    },
    "oName": {
      "singular": "nostr curated list",
      "plural": "nostr curated lists"
    },
    "oTitle": {
      "singular": "Nostr Curated List",
      "plural": "Nostr Curated Lists"
    },
    "description": "A list that is created according to the DCoSL protocol."
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
