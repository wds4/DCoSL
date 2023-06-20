```json
{
  "wordData": {
    "slug": "relationshipType_isASubcategoryOf",
    "version": "sandbox",
    "name": "relationship type: is a subcategory of",
    "title": "Relationship Type: Is a Subcategory Of",
    "wordTypes": ["relationshipType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "relationshipType_isASubcategoryOf",
          "version": "sandbox"
        }
      }
    }
  },
  "relationshipTypeData": {
    "slug": "isASubcategoryOf",
    "name": "is a subcategory of",
    "title": "Is a Subcategory Of",
    "description": "intended to be used to organize the tree of topics in the Pretty Good Curated Nostr Channels app",
    "wordFromAllowedWordTypes": ["nostrTopic"],
    "wordToAllowedWordTypes": ["nostrTopic"]
  }
}
```

This was broadcast to nostr using the following event:

```json
{
    "content": "{\"wordData\":{\"slug\":\"relationshipType_isASubcategoryOf\",\"version\":\"sandbox\",\"name\":\"relationship type: is a subcategory of\",\"title\":\"Relationship Type: Is a Subcategory Of\",\"wordTypes\":[\"relationshipType\"],\"metaData\":{\"nostr\":{\"stewardPubkey\":\"c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa\",\"uniqueIDs\":{\"slug\":\"relationshipType_isASubcategoryOf\",\"version\":\"sandbox\"}}}},\"relationshipTypeData\":{\"slug\":\"isASubcategoryOf\",\"name\":\"is a subcategory of\",\"title\":\"Is a Subcategory Of\",\"description\":\"intended to be used to organize the tree of topics in the Pretty Good Curated Nostr Channels app\",\"wordFromAllowedWordTypes\":[\"nostrTopic\"],\"wordToAllowedWordTypes\":[\"nostrTopic\"]}}",
    "kind": 9902,
    "tags": [
        [
            "c",
            "concept-graph-testnet-902"
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
            "relationshipType_isASubcategoryOf"
        ]
    ],
    "created_at": 1687300161,
    "pubkey": "e5272de914bd301755c439b88e6959a43c9d2664831f093c51e9c799a16a102f",
    "id": "907d13f442bdae9c6b12aa27e8d424bdf009dc2e8785a6eee915297a4fd7c849",
    "sig": "9023b1eff3f3155142969239db988505ffce56825a684fb01f009be973d5b3d7352abc5c00f33c401a8e132abf32bb7c69b3d1eed8c72f1ea0b3e838452d331b"
}
```
