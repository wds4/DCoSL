
`isASubsetOf` connects sets and subsets. It is one of the essential links in a class thread. 

`IsASubsetOf` connects wordType to wordType and is not part of a class thread. It can be useful to establish `IsASubsetOf` if the relevant wordTypes have been created byt the coresponding superset nodes have not yet been established.

```json
{
  "wordData": {
    "slug": "relationshipType_IsASubsetOf",
    "name": "relationship type: is a subset of",
    "title": "Relationship Type: Is a Subset Of",
    "wordTypes": ["relationshipType"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "relationshipType_IsASubsetOf"
        }
      }
    }
  },
  "relationshipTypeData": {
    "slug": "is_a_subset_of",
    "name": "is a subset of",
    "title": "Is a Subset Of",
    "description": "similar to isASubsetOf except that it connects wordTypes, not sets or subsets.",
    "wordFromAllowedWordTypes": ["wordType"],
    "wordToAllowedWordTypes": ["wordType"],
  }
}
```
