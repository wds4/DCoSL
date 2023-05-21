# The Grapevine: important concepts

`The grapevine` is the term used for a web of trust that follows DIP-01.

## Context trees and inheritance of trust scores

Trust is contextual. Who manages the list of contexts? Your WoT, via DCoSL.

Context can be coarse grained (Alice trusts Bob to evaluate products classified as electronics) or fine grained (Alice trusts Bob to evaluate products classified as smartphones, or iPhones, or maybe the iPhone 13). So some contexts are subsets of others. A list of contexts, plus a list of context relationships (iPhones is a subcategory of smartphones) is a context tree.

Context trees are important for calculation of trust scores using inheritance. Suppose Alice wants to know whether Bob can be trusted to rate iPhone 13. Her web of trust indicates Bob is trusted on the generic topic of electronics, but no one has commented whether he can be trusted in the more specific contexts. In this case, his calculated trust score in the context of electronics would be 'inherited' from the generic context, electronics, to all of its subcategories. If users later add ratings regarding Bob's trustworthiness in the more specific context of iPhones, then the more specific (coarse grained) attestations override the more generic (fine grained) attestations.

In this way, a curated context tree can grow gradually over time from immature with few details to more mature with lots of details without anything breaking. And the system functions, regardless whether the amount of knowledge that Alice's WoT is able to feed to her regarding Bob is sparse (few attestations) or not (many attestations).

## Confidence (certainty) of trust scores

Every trust score is accompanied by a number indicating the confidence in that score. Alice may think Bob is as smart as Einstein; she may be certain of that because she has known him a long time or because lots of her friends have told her so, or she may base this evaluation off of one brief encounter, so is not certain of it. When inherited trust scores are overridden by fine grained (more specific) attestations, the confidence of each score is an integral part of that calculation.

Also: a user's contextual influence is a combination of contextual trust score (higher trust means more influence) as well as confidence in that score (higher confidence also means more influence).

# DIPs 200-299: the Grapevine

- [DIP-200](200.md) first grapevine DIP

- [DIP-201](201.md): the Context tree and inheritance of average scores
