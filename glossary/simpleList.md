simple list
======

A list without any of the bells and whistles characteristic of a [complex list](complexList.md). 

The specification of a simple list does not include a way to partition list items into subsets. In addition, the available fields for a list and a list item are fixed and cannot be customized. In [Pretty Good Apps](https://github.com/wds4/pretty-good), lists are provided with three text fields (`name.singular`, `name.plural`, `description`) while list items are provided with two (`name`, `description`).

Example of a simple list of widgets, following the conventions of [DIP-104](../dips/conceptGraph/104.md):

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
    "description": "lorem ipsum"
  }
}
```

Example of an item on the list of widgets:

```json
{
  "wordData": {
    "wordTypes": ["widget"],
  },
  "widgetData": {
    "name": "my awesome widget",
    "description": "lorem ipsum"
  }
}
```
