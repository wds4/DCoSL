DIP-100
======

Simple Lists
------------------------------

`lists` and `listItems` are the basic building blocks of DCoSL. 

According to this DIP, users are given the ability to manage individually as well as to crowdsource simple lists.

## General principle

a `list` is a JSON with three fixed fields, as in the example below: 

```
{
  listData: {
    name: {
      singular: 'nostr relay',
      plural: 'nostr relays',
    },
    description: 'lorem ipsum',
  }
}
```

a `listItem` is a JSON with two fixed fields, as in the following example:

```
{
  listItemData: {
    name: 'wss://relay.damus.io',
    description: 'lorem ipsum',
  }
}
```

## Abstraction

The statement: 

```
(listItem) is a member of (list)
```

with parentheses denoting a cryptographic identifier, is fundamental to DCoSL, in the same way that the membership relation

```a ∈ b```

is fundamental to set theory, and thus to all of methematics. 

Although not necessary for our purposes, we could carry the abstraction further:

```
(thing) is a member of (thing)
```

where designations `list` and `listItem` are implied by the relationship.
