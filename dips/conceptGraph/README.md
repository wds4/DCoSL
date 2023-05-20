# The Concept Graph: Important Concepts

## Context trees and inheritance of trust scores

Trust is contextual. Who manages the list of contexts? Your WoT, via DCoSL.

Context can be coarse grained (Alice trusts Bob to evaluate products classified as electronics) or fine grained (Alice trusts Bob to evaluate products classified as smartphones, or iPhones, or maybe the iPhone 13). So some contexts are subsets of others. A list of contexts, plus a list of context relationships (iPhones is a subcategory of smartphones) is a context tree.

Context trees are important for calculation of trust scores using inheritance. Suppose Alice wants to know whether Bob can be trusted to rate iPhone 13. Her web of trust indicates Bob is trusted on the generic topic of electronics, but no one has commented whether he can be trusted in the more specific contexts. In this case, his calculated trust score in the context of electronics would be 'inherited' from the generic context, electronics, to all of its subcategories. If users later add ratings regarding Bob's trustworthiness in the more specific context of iPhones, then the more specific (coarse grained) attestations override the more generic (fine grained) attestations.

In this way, a curated context tree can grow gradually over time from immature with few details to more mature with lots of details without anything breaking. And the system functions, regardless whether the amount of knowledge that Alice's WoT is able to feed to her regarding Bob is sparse (few attestations) or not (many attestations).

## Confidence (certainty) of trust scores

Every trust score is accompanied by a number indicating the confidence in that score. Alice may think Bob is as smart as Einstein; she may be certain of that because she has known him a long time or because lots of her friends have told her so, or she may base this evaluation off of one brief encounter, so is not certain of it. When inherited trust scores are overridden by fine grained (more specific) attestations, the confidence of each score is an integral part of that calculation.

Also: a user's contextual influence is a combination of contextual trust score (higher trust means more influence) as well as confidence in that score (higher confidence also means more influence).

## the special utility for graphs (and graph databases) in DCoSL

A graph is a collection of nodes and edges, with each edge being a connection between two nodes. A graph can therefore be specified in full using no more than <i>two simple lists</li>, each one of which can be managed using DCoSL! (May want to have a thid list for types of edges, and perhaps a fourth list for types of nodes. But in many cases those lists would be managed by the developer, leaving only two lists to be curated by the WoT.)

Graphs have the attractive quality that they can be combined using basic set operators: union, intersection, etc. So if my WoT approves of Graph A as well as Graph B, then Alice can combine Graphs A and B into Graph C through the union operation. Example: Graph A is Verifiable Credential backbone curated by users who specialize in Verifiable Credentials, and Graph B is an auxiliary Verifiable Credential for nurse practitioners, curated by users who are nurse practitioners, but which assumes the VC backbone to be curated separately.

In the DIPs that follow, several specialized graphs will be defined, each with specialized edge types and node types that are defined within the DIP.
<li>a graph for an individual Concept</li>
<li>a graph for the subset tree for a particular concept</li>
<li>a graph for the Property Tree which defines the JSON Schema for a concept</li>
<li>a layer 1 Concept Graph, which shows the high level relationships between multiple Concepts</li>
<li>a graph for a Context Tree, which is used by the grapevine to calculate context-based scores by inheritance of default values from generic contexts to specific contexts</li>

Each of the above types of graphs can be specified by the developer, can be managed by hand by the individual user, or can be farmed out to one's web of trust.

- [DIP-100](100.md) basic use of graphs
