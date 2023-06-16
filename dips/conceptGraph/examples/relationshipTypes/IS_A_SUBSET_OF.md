
`isASubsetOf` connects sets and subsets. It is one of the essential links in a class thread. 

`IS_A_SUBSET_OF` connects wordType to wordType and is not part of a class thread. It can be useful to establish `IS_A_SUBSET_OF` if the relevant wordTypes have been created byt the coresponding superset nodes have not yet been established.

```json
{
  "wordData": {
    "slug": "relationshipType_IS_A_SUBSET_OF",
    "wordTypes": ["relationshipType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "relationshipType_IS_A_SUBSET_OF"
        }
      }
    }
  },
  "relationshipTypeData": {
    "slug": "IS_A_SUBSET_OF",
    "name": "IS_A_SUBSET_OF",
    "title": "IS_A_SUBSET_OF",
    "description": "similar to isASubsetOf except that it connects wordTypes, not sets or subsets.",
    "wordFromAllowedWordTypes": ["wordType"],
    "wordToAllowedWordTypes": ["wordType"],
  }
}
```
