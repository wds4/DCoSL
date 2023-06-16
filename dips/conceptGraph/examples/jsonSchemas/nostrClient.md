```json
{
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
