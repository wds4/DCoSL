complex list
======

A [simple list](simpleList.md) with at least one of the following additional features as part of the list specification.

Additional features include: 
- properties of lists and list items can be customized by hand by the user, +/- the option of crowdsourcing
- partitioning of list items into subsets can be managed by the user either directly or through crowdsourcing

The ability to partition into subsets could be subsumed into the definition / specification of the list. Alternatively, partitioning into subsets could be managed independently of the list definition or specification.

Example of a complex list for widgets, followed by an item on the list of widgets. Note that the list specification defines `color` as an additional property.

```json
{
  "wordData": {
    "wordTypes": ["list"],
  },
  "listData": {
    "name": {
      "singular": "widget",
      "plural": "widgets",
    },
    "description": "lorem ipsum",
    "properties": {
      "color": {
        "type": "string"
      }
    }
  }
}
```

```json
{
  "wordData": {
    "wordTypes": ["widget"],
  },
  "widgetData": {
    "name": "my awesome widget",
    "description": "lorem ipsum",
    "color": "blue",
  }
}
```


