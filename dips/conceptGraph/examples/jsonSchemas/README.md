Examples of json schemas
=====

# graphs

There are two versions of graphs, a 'compact' version (version 1) and a 'verbose' version (version 2).

In each version, `graphData` contains two primary properties: an array called `nodes` and an array called `relationships`.

## verbose 

This is the standard version.

nodes: Elements of the array: `graphData.nodes` are objects, each one of which contains one or more unique identifiers for one word.

relationships: Elements of the array: `graphData.relationships` are objects, formatted as per this example:

```json
{
    "nodeFrom": {
        "slug": "dogs"
    },
    "relationshipType": {
        "slug": "isASubsetOf"
    },
    "nodeTo": {
        "slug": "animals"
    },
}
```

## compact

nodes: Elements of the array: `graphData.nodes` are strings, each one of which is the unique identifier of one word. 

relationships: Elements of the array: `graphData.relationships` are themselves arrays, each one of which is a 3-tuple containing 3 items, each one of which is the unique identifier of one word, in the following order:
- nodeFrom
- relationshipType
- nodeTo

The list of allowed identifier types is located in `graphData.uniqueIdTypes`, which is an array and takes values: `nostrEventID` (typically), `nostrStewardPubkeyPlusSlug`, `ipfsHash`, `ipnsName`, or `slug`. If `slug` is indicated, then there must be a location to look up the word using the slug, typically within another graph. (Still need to decide how to specify the graph.)

The above example would be converted to:

```json
["dogs", "isASubsetOf", "animals"]
```
