simple list
======

## Definition

In mathematical terms, a simple list is an unordered set. Any given `item` either is or is not on any given list (an element of that set). Simple refers to the fact that there are no bells and whistles, like division of items into subsets, special properties for items of the list, etc. A list with bells and whistles like sets or properties is referred to as a `complex list`. Of note, a complex list can be constructed out of a simple list through the use of additional 'auxiliary' lists, like a list of associated properties or a list of associated subsets.

## simple vs complex lists

A `simple list` is a list without any of the bells and whistles characteristic of a [complex list](complexList.md). 

The specification of a simple list does not include a way to partition list items into subsets. In addition, the available fields for a list and a list item are fixed and cannot be customized. In [Pretty Good Apps](https://github.com/wds4/pretty-good), lists are provided with three text fields (`name.singular`, `name.plural`, `description`) while list items are provided with two (`name`, `description`).

## Everything can be broken down into simple lists

Consider the following examples of simple lists:
<li>a list of nostr relays</li>
<li>a list of reliable nostr relays</li>
<li>a list of subsets of nostr relays: free, paid, with filters, without filters, etc</li>
<li>a list of relationships between subsets: A is a subset of B, B is a subset of C, etc.</li>
<li>a list of user profile attributes: display_name, picture_url, about, location, twitterHandle, etc</li>
<li>a list of javascript data types: string, object, array, boolean, etc.</li>
<li>a list of lists that could be farmed out to one's web of trust</li>

<br />

A data model (e.g. a verifiable credential), an ontology, a schema or a context tree: these can all be built out of simple lists, each one of which can be curated. Imagine if your users no longer had to rely upon the World Wide Web Consortium (W3C) to manage a standard. With DCoSL, your users can farm out curation of any standard in question to their web of trust. Updates can potentially occur 24/7/365, not whenever the committee meets.

From a practical perspective, the challenge to the developer becomes which list(s) to curate and in what order to rollout list curation. The impact of DCoSL may not be apparent after curation of just one list. But as more lists are added, and more DIPs are adopted, the impact and significance will grow significantly.

## Examples

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

