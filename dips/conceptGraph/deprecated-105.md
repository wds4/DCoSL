DIP-105
======

Publication of a list or a list item (DIP-100) or a word (DIP-104) over nostr
------------------------------

See also [DIP-200](../grapevine/200.md) for publication of a rating over nostr.

This DIP proposes conventions for packaging a `list` or a `list item` (as defined by [DIP-100](100.md)) or a `word` (as defined by [DIP-104](104.md)) as a nostr event for publication over nostr.

The list, list item or word is converted from JSON to a string and placed into the nostr event `content` field.

## kinds and tags

They are published as a Regular Event as per [NIP-16](https://github.com/nostr-protocol/nips/blob/master/16.md) with kind anywhere in the range 9000 to 9999. (Regular Events can be anywhere in the range 1000 - 9999, but kinds below 9000 are avoided to minimize potential collisions with other NIPs.)

- kind 9901, with tag: `["c", "concept-graph-testnet-901"]`
- kind 9902, with tag: `["c", "concept-graph-testnet-902"]`
- mainnet is anticipated to launch using kind 9001, tag: `["c", "concept-graph-001"]`

### Required tags

| tag            | description                      | values |
| ---------------- | -------------------------------- | -------|
| `c`              | indicates concept graph          | `concept-graph` |
| `t`              |  task | `createInstance`, `createWord` |

### tasks

| task slug            | description                      |
| ---------------- | -------------------------------- |
| `createInstance` (= `createItem` = `createListItem`)  | add a word to an existing concept or set |
| `createWord` | add a word |

When the task is `createInstance`, at least one, preferably both, of the following tags must be published to identify the parent list, of which the word currently being published is an item:

| tag            | description                      |
| ---------------- | -------------------------------- |
| `s`              | slug of the parent concept OR of a set  |
| `e`              |  nostr event id of the parent concept |

If the `e` and the `s` tags are missing from `createInstance` task, then the task is converted to a simple `createWord`.

Example 1: packaging the creation of the list of `widgets` from the example in [DIP-01](../01.md):

```json
{
    "id": "ae641d5606f3ec710b135678810d4256fd2e92022896ca58d194c361c46d81f9",
    "content": "{ ... }",
    "kind": 9901,
    "tags": [
        ["c", "concept-graph-testnet-901"],
        ["t", "createInstance"],
        ["s", "nostrCuratedList"]
    ],
    ...other fields
}
```

Example 2: packaging the word `first test widget entry` as an item on the list of `widgets`, from the example in [DIP-01](../01.md):

```json
{
    "kind": 9901,
    "tags": [
        ["c", "concept-graph-testnet-901"],
        ["t", "createInstance"],
        ["e", "ae641d5606f3ec710b135678810d4256fd2e92022896ca58d194c361c46d81f9"],
        ["s", "widget"]
    ],
    "content": "{\"widgetData\":{\"name\":\"first test widget entry\",\"slug\":\"firstTestWidgetEntry\",\"description\":\"a sample entry to the list of widgets\"}}",
    ...other fields
}
```

# Search

To search for lists, list items or words, use the following filters:

```
work in progress
```


