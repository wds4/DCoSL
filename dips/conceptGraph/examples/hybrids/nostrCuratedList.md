This is a combination `wordTYpe` and `jsonSchema`. As a `wordType`, tecnically the issuance of this word is a `declaration`.

Basically I've taken the word type and the json schema for nostrCuratedList, put them together into one word, changed the slug name (so I don't confuse it with the original nostrCuratedList) and added a version. 

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
  }
}
```
