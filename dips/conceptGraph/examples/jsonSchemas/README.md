Examples of json schemas
=====

## graphs

There are two versions of graphs, a 'compact' version (version 1) and a 'verbose' version (version 2).

### compact

This is an alternate, more compact format for the `graph` word type. Different properties in `graphData` than in the first example. Not sure if I will make this a distinct graph format with a different name or just an alternate implementation of the `graph` concept.

### verbose 



`graphData.uniqueIdTypes` takes values: `nostrEventID` (typically), `nostrStewardPubkeyPlusSlug`, `ipfsHash`, `ipnsName`, or `slug`. If `slug` is indicated, then there must be a location to look up the word using the slug, typically within another graph; would need to decide how to specify the graph.
