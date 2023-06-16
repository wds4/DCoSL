# sample graph

```json
{
  "wordData": {
    "slug": "sampleGraph",
    "wordTypes": ["graph"],
    "metaData": {
      "nostr": {
        "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
        "uniqueIDs": {
          "slug": "sampleGraph"
        }
      }
    }
  },
  "graphData": {
    "slug": "sampleGraph",
    "nodes": [
      {
        "slug": "word",
        "nostr": {
          "eventID": "4a5517d25ebae34b9794f1b8d4dba0681f7ff7297bacbc29de2c915695c53bfe",
          "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
          "slug": "word",
        },
        "ipfs": {
          "ipfs": null,
          "ipns": null
        }
      }
    ],
    "relationships": [],
    "relationshipTypes": [],
    "importedGraphs": []
  }
}
```

Consider the first element of the array `graphData.nodes`:

```json
{
  "slug": "word",
  "nostr": {
    "eventID": "4a5517d25ebae34b9794f1b8d4dba0681f7ff7297bacbc29de2c915695c53bfe",
    "stewardPubkey": "c51a542e4f93afe6f45e5bef002f7a0efcc0a47460a736654c0bee5402c482fa",
    "slug": "word",
  },
  "ipfs": {
    "ipfs": null,
    "ipns": null
  }
}
```

The top line, `slug`, is what this word will be referred to locally. The data inside `nostr` and `ipfs` indicate how to retrieve the word from the nostr and the ipfs networks, respectively (although the data may be empty, as in this case). `nostr.eventID` would retrieve a specific version of this word, whereas `nostr.stewardPubkey` and `nostr.slug` are sufficient to extract all versions of this word, with the most recently published version (going by created_by) being considered to be the most up to date version. The local user is free to decide whether to use a fixed version (`nostr.eventID`) or the variable version, which of course requires a certain degree of trust in the stweard profile. Note also that the `slug` used locally and the `slug` used by the word's author (the steward profile) may or may not be the same. In this way, words and concepts can be shared across users of multiple languages. For words stored in ipfs, the slug is simply extracted from the word itself and is not specified here.
