DIP-104
======

words and wordTypes
------------------------------

## General principle

assume JSON

### words

Following [DIP-02](../02.md), Every node and every relationship in the graph database will be associated with one or more cryptographic identifiers, which are (presumably) globally unique. In addition, human-readable identifiers may be used, with one of the concept graph criteria being that all such identifiers must be unique within a concept graph.

The DCoSL convention for nodes: Wherever possible, we will format data files using JSON, with each node representing a single JSON object. Other types of nodes with other formats (images, other data types such as XML or CSV, etc) will be assumed in principle to exist.

Nodes that follow the DCoSL convention will be referred to as a `word`. Each word will have a top-level property: `wordData` with mutable, human-readable unique identifiers. Mutable but non-human-readable unique identifiers will be found under `metaData`. For example:

```
{
  wordData: {
    slug: 'fooBar_63b621',
    name: 'foo bar',
    title: "Foo Bar',
  },
  ...
  metaData: {
    nostrEventID: '7380e72c0e029f55cff42cf4d437ea98c1d5bd9d206345e564d4c4511163b621',
  },
}
```

In the above example, name and title are not required to be unique within the concept graph. However, wordData.slug must be unique. To enfore uniqueness, the convention will be to create the slug from the name, using camel case, with underscore followed by the last 6 characters of whatever non-human-readable mutableidentifier is being used.

### wordTypes

`Words` (defined above) will be divided into `word types`. Any word can be (and usually will be) of more than one word type. Word types will be indicated as in the example below. For each word type `foo`, there will be a top-level object property called `fooData`.

```
{
  wordData: {
    slug: 'myWidget_63b621',
    wordTypes: [ 'word', 'widget' ],
  },
  widgetData: {
    name: 'my widget',
    title: "My Widget',
  },
  ...
  metaData: {
    nostrEventID: '7380e72c0e029f55cff42cf4d437ea98c1d5bd9d206345e564d4c4511163b621',
  },
}
```

For each word type, properties `name`, `title`, and `description` will be made available by default but will not be required. Note that in the above example, name and title are present under widgetData and have been removed from wordData.

Note that the inclusion of 'word' as an item in wordData.wordTypes is implied and may be excluded without generating an error.

An example of a word with multiple word types:

```
{
  wordData: {
    slug: 'myWidget_63b621',
    wordTypes: [ 'word', 'animal', 'dog' ],
  },
  animalData: {
    animalType: 'dog',
  },
  dogData: {
    name: 'Fido',
  },
  ...
  metaData: {
    nostrEventID: '7380e72c0e029f55cff42cf4d437ea98c1d5bd9d206345e564d4c4511163b621',
  },
}
```

Note that in the above example, the set `dogs` is a subset of `animals`.
