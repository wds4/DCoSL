# DIPs: DCoSL implementation proposals

The basic starting point (as discussed in concept graph readme? or DCoSL readme? or glossary? or create a DIP-0* ?) is to represent data as a graph, with nodes and edges. (State elsewhere: Graph databases like neo4j could be considered but are not necessary and not necessarily recommended and probably not beneficial until later stages with large concept graphs.)

The special role of graphs in the DCoSL protocol is discussed in [concept graph](conceptGraph/README.md).

DIPs (DCoSL implementation proposals) are categorized into three blocks: the core protocol, the concept graph, and the grapevine.

## [basic principles: DIPs 00 - 99](coreProtocol)

Basic starter DIPs. 

### implementations:

- DIP-00: [Pretty Good Apps](https://github.com/wds4/pretty-good), nostr - settings - relays
- DIP-01: [Pretty Good Apps](https://github.com/wds4/pretty-good), the Curated Lists app

## [the concept graph: DIPs 100-199](conceptGraph)

There will be a natural progression from simple lists, to complex lists, to concepts, to the concept graph.

## [the grapevine: DIPs 200-299](grapevine)

Describes the calculation of context-based user influence

## [networking: DIPs 1000-1999](networking)

publication and retrieval of data to/from the nostr network

## [DIP infinity, aka Circular DCoSL](conceptGraph/infinity.md)

a state of enlightenment where the implementation of DCoSL is itself crowdsourced using DCoSL.

