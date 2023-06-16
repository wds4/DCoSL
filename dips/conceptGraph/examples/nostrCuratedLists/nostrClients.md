nostr clients
=====



```json
{
    "nostrCuratedListData": {
        "name": {
            "singular": "nostr client",
            "plural": "nostr clients"
        },
        "title": {
            "singular": "Nostr Client",
            "plural": "Nostr Clients"
        },
        "slug": {
            "singular": "nostrClient",
            "plural": "nostrClients"
        },
        "description": "a list of all nostr clients",
        "propertyPath": "nostrClientData"
    },
    "jsonSchemaData": {
        "description": "This is the JSON Schema used to create and validate object files for the representation of instances of the list of nostr clients",
        "name": "json schema for an instance of nostr client",
        "title": "JSON Schema for an Instance of Nostr Client",
        "type": "object",
        "required": [
            "nostrClientData"
        ],
        "definitions": {},
        "properties": {
            "nostrClientData": {
                "type": "object",
                "name": "nostr client data",
                "title": "Nostr Client Data",
                "description": "data about this nostr client",
                "require": true,
                "required": [
                    "name"
                ],
                "definitions": {},
                "properties": {
                    "name": {
                        "type": "string",
                        "require": true
                    },
                    "title": {
                        "type": "string",
                        "require": false
                    },
                    "slug": {
                        "type": "string",
                        "require": false
                    },
                    "description": {
                        "type": "string",
                        "require": false
                    }
                }
            }
        }
    }
}
```

Note that the above example:
- wordData has been omitted. If it had been included, it would have included the following information:

```json
{
  "wordData": {
    "slug": "nostrCuratedList_nostrClients",
    "wordTypes": ["nostrCuratedList", "jsonSchema"],
    "metaData": {
    
    }
  }
}
```

- jsonSchema has been included in the same word. This is nonstandard. Normally the json schema would be a separate word.
