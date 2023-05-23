# DCoSL: Decentralized Curation of Simple Lists

## Preamble

DCoSL is a work in progress. I am basically starting with a vision for the desired end-state of a completely decentralized web (["DIP-infinity"](dips/infinity.md)) and working backwards from there to where we are now. As of 23 May 2023 I have the outline of a path and am working on filling in the details as much as possible. I am also very close to drawing a path from the current state of nostr (e.g. [NIP-51](https://github.com/nostr-protocol/nips/blob/master/51.md): Lists) to potential entry points into DCoSL ([DIP-105](nips/conceptGraph/105.md): Publication of list, list item, or word to nostr or [DIP-200](nips/grapevine/200.md): publication of a rating, endorsement or attestation to nostr). (Those DIPs have too much packed into them; need to break them up, perhaps.) The flexibility of the DCoSL approach means that once the path from nostr to DCoSL is complete, other onboarding pathways (not necessarily nostr-related) should be possible as well.

## Intro

DCoSL is a flexible protocol to guide the step-by-step construction of a decentralized web, with an emphasis on decentralized reputation and web of trust. Its design is inspired by the [nostr protocol](https://github.com/nostr-protocol/nostr). The protocol that follows is written to sit atop of nostr but could also be implemented in a nostr-independent fashion with minimal changes to the DCoSL protocol as currently specified.

The DCoSL protocol is based on the premise that the curation of a [simple list](glossary/simpleList.md) by one's web of trust should be considered not only the atomic unit of the decentralized web, but also its defining feature. DCoSL strives to turn a difficult and perhaps seemingly overwhelming challenge -- creation of a web of trust that lots of people actually use -- into a tractable one by breaking it down into bite size steps: one list at a time, and one DIP (DCoSL implementation proposal) at a time.

Just about anything can be expressed in terms of lists: a list of trusted lightning nodes, a list of nostr relays, a list of user properties (display_name, about, picture_url, etc), a list of nodes & a list of edges in a [graph database](glossary/graphDatabase.md), and so on. Multiple lists used together can result in a [complex list](glossary/complexList.md), with 'complex' referring to the fact that the list is imbued with special features like subsets, customized properties for items on the list, etc. Out of simple lists, data structures, protocols, etc can be constructed that are as basic or as sophisticated as they need to be. And with DCoSL, those can be managed in a truly decentralized fashion.

With DCoSL, developers build tools to allow users to farm out various decisions, whether large or small, to communities of users. By choosing a list or lists carefully, a magical thing can emerge called [loose consensus](glossary/looseConsensus.md): under the right circumstances, especially for lists that are not controversial, Alice's WoT and Bob's WoT, though they may not be identical, could very easily have significant overlap, and could very easily end up farming out the curation of said list(s) to the same small group of trusted list curators (who may simply be the only people with the time and inclination to curate this particular list!). Although not enforced or guaranteed (hence the term: 'loose'), for a large category of lists, Alice and Bob will end up using the exact same (or at least almost the same) list! Shared lists, shared protocols, shared data structures, shared language; these obviate the need for any centralized entity to build and maintain a platform.

The term [crowdsourcing](glossary/crowdsource.md) will be used to refer to curation of one or a group of simple lists where a high degree of loose consensus is expected. [Schemas](https://schema.org/docs/schemas.html), data models, verifiable credentials, standards, etc can be crowdsourced.

In the spirit of nostr, DCoSL is defined by a series of DIPs: DCoSL implementation proposals. Like nostr, a small handful of core DIPs go a long way. Most of the rest can be rolled out incrementally. Likewise, lists can be farmed out incrementally, allowing more and more design decisions to be placed under the control of user communities. In the long run, <i>even the management of the DCoSL protocol itself can be farmed out using the DCoSL protocol</i>, a state called `NIP-infinity` or `circular DCoSL` (this name paying homage to the notion of the 'circular economy').

# Why do we need DCoSL?

If the goal of Bitcoin is to decentralize the flow of value, it may be said that the goal of DCoSL (as well as nostr) are to decentralize the flow of information.

What is our vision for the decentralized web? Billions of people, millions of developers, free to associate and interact as they wish. As cypherpunks we strive to build tools to enable their spontaneous, dynamic organization into networks both large and small, with or without overlap, each one of which is capable of highly sophisticated intra-network communication and coordinated action, <i>without ever putting any one person, developer, or entity in charge of the tools for any given network</i>. Have we succeeded? We're making progress, but we're not there yet.

Consider all of the awesome things we can do on the internet today that we could not do just a few short decades ago. All the highly sophisticated ways that two human beings, on opposite sides of the planet, can find each other like needles in a haystack, connect and interact, peer to peer. We have data curation (Google search), eCommerce (Amazon, eBay), social media (Twitter, Facebook, Instgram), and more. Unfortunately, despite their peer to peer nature, these interactions are routed through increasingly large, centralized, powerful entities -- public and private -- that gain more and more power and control over individuals and society at large, to the detriment of us all. These centralized entities provide the shared consensus required for sophisticated, specialized peer to peer interactions. The goal of the decentralized web is to render these centralizing entities unnecessary. To provide the tools to build shared consensus, to reproduce these sophisticated p2p interactions, and more.

Open source software is a marked improvement over proprietary software, but is not a perfect answer to the above problems. Developers who manage repositories, committees that manage standards, continue to exercise control that is not always fully mitigated despite the benefits of open source such as the ability to fork projects which most users have neither the time, expertise, or motivation to carry out. One of the goals of DCoSL is to give users the option to farm out management of standards, libraries, protocols, etc to a decentralized web of trust, to give that option to users who don't necessarily know how to code, and to make that option as easy as clicking a button. 

When we no longer need today's centralized tech platforms, nor the standards bodies frequently associated with them, we will know we have succeeded.

# Why will DCoSL succeed where others have failed?

People have been trying to build webs of trust going back at least as far as 1991 when Phil Zimmerman released Pretty Good Privacy. Unfortunately, none have seemed to gain the sort of traction that was initially expected and desired. 

DCoSL strives to draw lessons from the success of bitcoin and nostr, each of which created or accomplished something previously thought by many to be impossible, or at least infeasible. Neither bitcoin nor nostr were the product of some shiny new technology. Each uses tools that had been laying around for quite some time. Simplicity of the starting point. The bitcoin consensus rules have no extraneous details. The nostr core protocol is as stripped down as can be. I think lightning is cool; but the consensus rules, to their credit, do not obligate the use of lightning. You may think kademlia is cool, or some decentralized identifier (DID) implementation is particularly cool, and you may be right. But nostr, to its credit, does not obligate the developer or the user to commit to these or to much else. Most NIPs are optional. 

The DCoSL protocol is designed in the same way. No matter how awesome are any of the DIPs beyond the first few, they are optional. In many cases, for many DIPs, there may be multiple similar but not necessarily identical ways to achieve the same goal ('DIP-xx-equivalents'). DCoSL does not require interacting users to implement the same DIPs, or to implement them in the same way. This is part of loose consensus: on any given list, consensus is highly likely to happen, but if it doesn't happen or if it's not perfect, that's OK. Lack of consensus on some minor detail will not require Alice and Bob to segregate into two nonoverlapping, noninteracting, completely separated networks (which is what typically happens if some open source platform gets forked).

# Why has DCoSL not been done before?

DCoSL requires an understanding and appreciation of several key concepts (below), most notably loose consensus and DIP-infinity (aka circular DCoSL) and a belief that such things are both possible and desirable. It can be challenging to build up or to convey any one of these concepts without the other concepts already in place.

In addition, DCoSL requires a clear starting point and a roadmap. DIP-00 is an easy starting point for any project. DIP-01 is a more difficult hurdle: it is relatively easy to describe but requires considerably more work for the developer to implement. Subsequent DIPs provide the building blocks of a roadmap. Although the benefits of early stage DIPs may be slight, the potential benefits of additional DIPs and a maturing DCoSL ecosystem are enormous. But no developer would ever start building these tools and following this roadmap without some assurance that the big picture is a sensible one. Hopefully, this document will be able to convey this roadmap along with its big picture including its endpoint, DIP-infinity.

In addition to the above, some may have philosophic difficulties with the starting point, DIP-00 (for any curated list, there is no universal, 'correct' master list), analogous to the philosophic difficulties of the number zero of some societies in ages past. So some maybe gotta get past that.

# Important concepts

## Everything can be broken down into simple lists

In mathematical terms, a simple list is an unordered set. Any given `item` either is or is not on any given list (an element of that set). Simple refers to the fact that there are no bells and whistles, like division of items into subsets, special properties for items of the list, etc. A list with bells and whistles like sets or properties is referred to as a `complex list`. Of note, a complex list can be constructed out of a simple list through the use of additional 'auxiliary' lists, like a list of associated properties or a list of associated subsets.

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

## Loose Consensus 

If the contents of a list are not particularly polarizing or controversial (and most of them aren't), then there is a good chance that Alice's WoT and Bob's WoT will come up with the same, or at least very similar, lists. This is known as <i>loose consensus</i>. Much of the power of DCoSL comes from its ability to generate loose consensus.

Alice's WoT and Bob's WoT, though they are not identical, are very likely to have significant overlap. For any given list, although there is no guarantee, there is a good chance that Alice and Bob will end up using the exact same (or at least almost the same) list! This is a vitally important attribute, one that I call loose consensus. You'll want to think deeply about loose consensus before incorporating decentralized list curation to your app.

In some cases, a particularly controversial or politicized list may generate loose consensus that segregates by community.

The term `crowdsource` will be used to refer to curation of one or of a collection of simple lists using DCoSL protocol where a high degree of loose consensus is expected, at least within a given community. Schemas, verifiable credentials, etc can be said to be 'crowdsourced' via the DCoSL protocol, in each case through curation of a small handful of simple lists. One of the major challenges to the developer will be to write code that doesn't break when Alice and Bob maintain lists that do not match. Crowdsourcing one or a small handful of lists at a time should mitigate this difficulty

## DIP-infinity (aka circular DCoSL)

The DCoSL protocol itself can be expressed as a bunch of lists, and those lists can be managed via DCoSL. When the entire protocol is managed in this decentralized fashion, this is called DIP-infinity, or circular DCoSL (because DCoSL is being used to define DCoSL).

# Protocol specification 

DIPs (DCoSL implementation proposals) are categorized into three blocks: the core protocol, the concept graph, and the grapevine.

## [DCoSL Core Protocol: DIPs 00 - 99](https://github.com/wds4/DCoSL/tree/main/dips)

A selection of important DIPs is below. DIP-00 should be straightforward to implement in many cases. DIP-01 (without any additional DIPs) can be implemented without too much difficulty, although the rationale for doing so may not become apparent until many subsequent DIPs are also implemented. See [Pretty Good Apps](https://github.com/wds4/pretty-good) (specifically, the Curated Lists app) for an example of DIP-01 in conjunction with (long list of other DIPs). However, implementing just one or a few DIPs at a time is generally recommended from a developer perspective, with each DIP (possibly a small handful) being its own individual milestone. Easier to coordinate a team with clearly defined milestones.

- [DIP-00](dips/00.md): Lists are curated independently by each user. There is no universal, preferred or 'correct' list.

Each user is at the center of his or her web of trust, and each user's lists are curated independently.

- [DIP-01](dips/01.md): Rely on explicit attestations rather than scraped data.

- [DIP-02](dips/02.md): Use cryptographic identifiers for lists and list items.

- [DIP-03](dips/03.md): Representation of a graph using a small handful of simple lists.

The special role of graphs in the DCoSL protocol is discussed in [concept graph](dips/conceptGraph/README.md).

## [the concept graph: DIPs 100-199](https://github.com/wds4/DCoSL/tree/main/dips/conceptGraph)

There will be a natural progression from simple lists, to complex lists, to concepts, to the concept graph.

## [the grapevine: DIPs 200-299](https://github.com/wds4/DCoSL/tree/main/dips/grapevine)

Describes the calculation of context-based user influence

## DIP infinity, aka Circular DCoSL

The DCoSL protocol is used to curate itself. Also referred to as `Circular DCoSL`, a phrase that pays homage to the 'circular economy' of bitcoin.

# Notes

Considering changing DCoSL to WeCoSL: Web-enabled Curation of Simple Lists, changing DIPs to WIPs, and changing my profile pic to Devo.

