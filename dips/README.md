# DIPs: DCoSL implementation proposals

The basic starting point (as discussed in concept graph readme? or DCoSL readme? or glossary? or create a DIP-0* ?) is to represent data as a graph, with nodes and edges. (State elsewhere: Graph databases like neo4j could be considered but are not necessary and not necessarily recommended and probably not beneficial until later stages with large concept graphs.)

DIPs (DCoSL implementation proposals) are categorized into three blocks: the core protocol, the concept graph, and the grapevine.

## [core protocol: DIPs 00 - 99](coreProtocol)

A selection of important DIPs is below. DIP-00 should be straightforward to implement in many cases. DIP-01 (without any additional DIPs) can be implemented without too much difficulty, although the rationale for doing so may not become apparent until many subsequent DIPs are also implemented. See [Pretty Good Apps](https://github.com/wds4/pretty-good) (specifically, the Curated Lists app) for an example of DIP-01 in conjunction with (long list of other DIPs). However, implementing just one or a few DIPs at a time is generally recommended from a developer perspective, with each DIP (possibly a small handful) being its own individual milestone. Easier to coordinate a team with clearly defined milestones.

- [DIP-00](dips/00.md): Lists are curated independently by each user. There is no universal, preferred or 'correct' list.

Each user is at the center of his or her web of trust, and each user's lists are curated independently.

- [DIP-01](dips/01.md): Rely on explicit attestations rather than scraped data.

- [DIP-02](dips/02.md): Use cryptographic identifiers for lists and list items.

- [DIP-03](dips/03.md): Representation of a graph using a small handful of simple lists.

The special role of graphs in the DCoSL protocol is discussed in [concept graph](dips/conceptGraph/README.md).

## [the concept graph: DIPs 100-199](conceptGraph)

There will be a natural progression from simple lists, to complex lists, to concepts, to the concept graph.

## [the grapevine: DIPs 200-299](grapevine)

Describes the calculation of context-based user influence

## DIP infinity, aka Circular DCoSL

The DCoSL protocol is used to curate itself. Also referred to as `Circular DCoSL`, a phrase that pays homage to the 'circular economy' of bitcoin.



