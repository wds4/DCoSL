Examples of json schemas

## JSON Schemas

This is an alternate, more compact format for the `graph` word type. Different properties in `graphData` than in the first example. Not sure if I will make this a distinct graph format with a different name or just an alternate implementation of the `graph` concept.

`graphData.uniqueIdTypes` takes values: `nostrEventID` (typically), `nostrStewardPubkeyPlusSlug`, `ipfsHash`, `ipnsName`, or `slug`. If `slug` is indicated, then there must be a location to look up the word using the slug, typically within another graph; would need to decide how to specify the graph.
