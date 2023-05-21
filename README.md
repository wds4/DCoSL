# DCoSL: Decentralized Curation of Simple Lists

DCoSL is a simple, flexible protocol to guide construction of a decentralized web, using decentralized reputation and web of trust. Its design is inspired by the [nostr protocol](https://github.com/nostr-protocol/nostr), and couples well with nostr, but can be used in conjunction with any peer to peer platform or protocol.

The DCoSL protocol is based on the premise that the curation of a simple list by one's web of trust should be considered not only the atomic unit of the decentralized web, but also its defining feature. DCoSL strives to turn a difficult and perhaps seemingly overwhelming challenge -- creation of a web of trust that lots of people actually use -- into a tractable one by breaking it down into bite size steps: one list at a time, and one DIP (DCoSL implementation proposal) at a time.

Just about anything can be expressed in terms of lists: a list of trusted lightning nodes, a list of nostr relays, a list of user properties (display_name, about, picture_url, etc), and so on. Multiple lists used together can result in a `complex list`, with 'complex' referring to the fact that the list is imbued with special features like subsets, customized properties for items on the list, etc. Out of simple lists, data structures, protocols, etc can be constructed that are as basic or as sophisticated as they need to be. And with DCoSL, those can be managed in a truly decentralized fashion.

With DCoSL, developers build tools to allow users to farm out various decisions, whether large or small, to communities of users. By choosing a list or lists carefully, a magical thing can emerge called `loose consensus`: under the right circumstances, especially for lists that are not controversial, Alice's WoT and Bob's WoT, though they may not be identical, could very easily have significant overlap, and could very easily end up farming out the curation of said list(s) to the same small group of trusted list curators. Although not enforced or guaranteed (hence the term: 'loose'), for a large category of lists, Alice and Bob will end up using the exact same (or at least almost the same) list! Shared lists, shared protocols, shared data structures, shared language; these obviate the need for any centralized entity to build and maintain a platform.

In the spirit of nostr, DCoSL is defined by a series of DIPs: DCoSL implementation proposals. Like nostr, a small handful of core DIPs go a long way. Most of the rest can be rolled out incrementally. Likewise, lists can be farmed out incrementally, allowing more and more design decisions to be placed under the control of user communities. In the long run, <i>even the management of the DCoSL protocol itself can be farmed out using the DCoSL protocol</i>, a state called `NIP-infinity` or `circular DCoSL` (this name paying homage to the notion of the 'circular economy').

# Why do we need DCoSL?

If the goal of Bitcoin is to decentralize the flow of value, it may be said that the goal of DCoSL (as well as nostr) are to decentralize the flow of information.

Consider all of the awesome things we can do on the internet today that we could not do just a few short decades ago. All the highly sophisticated ways that two human beings, on opposite sides of the planet, can find each other like needles in a haystack, connect and interact, peer to peer. We have data curation (Google search), eCommerce (Amazon, eBay), social media (Twitter, Facebook, Instgram), and more. Unfortunately, despite their peer to peer nature, these interactions are routed through increasingly large, centralized, powerful entities -- public and private -- that gain more and more power and control over individuals and society at large, to the detriment of us all. These centralized entities provide the shared consensus required for sophisticated, specialized peer to peer interactions. The goal of the decentralized web is to render these centralizing entities unnecessary. To provide the tools to build shared consensus, to reproduce these sophisticated p2p interactions, and more.

Open source software is a marked improvement over proprietary software, but is not a perfect answer to the above problems. Developers who manage repositories, committees that manage standards, continue to exercise control that is not always fully mitigated despite the benefits of open source such as the ability to fork projects which most users have neither the time, expertise, or motivation to carry out. One of the goals of DCoSL is to give users the option to farm out management of standards, libraries, protocols, etc to a decentralized web of trust, to give that option to users who don't necessarily know how to code, and to make that option as easy as clicking a button. 

When we no longer need today's centralized tech platforms, nor the standards bodies frequently associated with them, we will know we have succeeded.

# Why will DCoSL succeed where others have failed?

People have been trying to build webs of trust going back at least as far as 1991 when Phil Zimmerman released Pretty Good Privacy. Unfortunately, none have seemed to gain the sort of traction that was initially expected and desired. 

DCoSL strives to draw lessons from the success of Bitcoin and nostr, each of which achieved goals that appeared by many to be unachievable. Neither Bitcoin nor nostr were the product of some shiny new technology. Each uses tools that had been laying around for quite some time. Simplicity of the starting point. The bitcoin consensus rules have no extraneous details. The nostr core protocol is as stripped down as can be. I think lightning is cool; but the consensus rules, to their credit, do not obligate the use of lightning. You may think kademlia is cool, or some decentralized identifier (DID) implementation is particularly cool, and you may be right. But nostr, to its credit, does not obligate the developer or the user to commit to these or to much else. Most NIPs are optional. 

The DCoSL protocol is designed in the same way. No matter how awesome are any of the DIPs beyoind DIP-0, they are optional. In many cases, for many DIPs, there may be multiple alternative ways to achieve the same goal ('DIP-xx-equivalents'). DCoSL does not require interacting users to implement the same DIPs, or to implement them in the same way. This is part of loose consensus: on any given list, consensus is highly likely to happen, but if it doesn't happen or if it's not perfect, that's OK. Lack of consensus on some minor detail will not require Alice and Bob to segregate into two nonoverlapping, noninteracting, completely separated networks (which is what typically happens if some open source platform gets forked).

# Why has DCoSL not been done before?

DCoSL requires an understanding and appreciation of several key concepts (below), most notably loose consensus and DIP-infinity (aka circular DCoSL) and a belief that such things are both possible and desirable. It can be challenging to build up or to convey any one of these concepts without the other concepts already in place.

In addition, DCoSL requires a clear starting point and a roadmap. DIP-0 is an easy starting point for any project. DIP-1 is relatively easy to describe but requires considerably more work for the developer to implement. Subsequent DIPs provide the building blocks of a roadmap. Although the benefits of early stage DIPs may be slight, the potential benefits of additional DIPs and a maturing DCoSL ecosystem are enormous. But no developer would ever start building these tools and following this roadmap without some assurance that the big picture is a sensible one. Hopefully, this document will be able to convey this roadmap along with its big picture.

In addition to the above, some may have philosophic difficulties with the starting point, DIP-0 (for any curated list, there is no universal, 'correct' master list), analogous to the philosophic difficulties of the number zero of some societies in ages past. So some maybe gotta get past that.

# Important concepts

## Everything can be broken down into simple lists

In mathematical terms, a simple list is an unordered set. Any given `item` either is or is not on any given list (an element of that set). Simple refers to the fact that there are no bells and whistles, like division of items into subsets, special properties for items of the list, etc. A list with bells and whistles like sets or properties is referred to as a `complex list`. Of note, a complex list can be constructed out of a simple list through the use of additional 'auxiliary' lists, like a list of properties or a list of subsets.

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

If the contents of a list are not particularly polarizing or controversial (and most of them aren't), then there is a good chance that Alice's WoT and Bob's WoT will come up with the same, or at least very similar, lists. This is known as <i>loose consensus</i>. The power of DCoSL is its ability to generate loose consensus.

Alice's WoT and Bob's WoT, though they are not identical, are very likely to have significant overlap. For any given list, although there is no guarantee, there is a good chance that Alice and Bob will end up using the exact same (or at least almost the same) list! This is a vitally important attribute, one that I call loose consensus. You'll want to think deeply about loose consensus before incorporating decentralized list curation to your app.

## DIP-infinity (aka circular DCoSL)

The DCoSL protocol itself can be expressed as a bunch of lists, and those lists can be managed via DCoSL. When the entire protocol is managed in this decentralized fashion, this is called DIP-infinity, or circular DCoSL (because DCoSL is being used to define DCoSL).

# How does DCoSL work?

merge following paragraphs: 

The basic idea of DCoSL is to provide tools to allow users to farm out decisions, major and minor, to their webs of trust, thereby decreasing reliance on dev teams, standards committees, etc. This is handled through curation of simple lists: an unordered set of elements, referred to here as `items`. Examples of simple lists: a list of nostr relays, a list of trusted lightning nodes, a list of properties for a user profile (name, display_name, picture_url, etc).

The basic premise of DCoSL is that the ability for a user to delegate curation of a simple list to the web of trust (DIP-0) should be considered the <i>defining feature</i> of the decentralized web. If a platform does not satisfy NIP-0, it is not part of the decentralized web. If it does satisfy NIP-0, then it should be considered as part of the decentralized web, even if only one single list qualifies.

The reason that DCoSL will succeed where previous attempts at webs of trust have fallen short is that DCoSL offers a strategy to take a complex, overwhelming problem and break it down into small steps. How? As developers, you can provide your users with the ability to delegate list curation to their webs of trust in bite sized chunks: <i>one list at a time</i> (or perhaps a small handful of lists at a time).

DCoSL relies heavily on graphs. Why? Because a graph can be specified in full using two simple lists: one list for nodes, and one list for edges. A data model (e.g. a verifiable credential), an ontology, a schema or a context tree: these can all be built out of simple lists, each one of which can be curated. 

# Who should implement this? How to get started?

Any developer working on any peer to peer platform, protocol, library, or tool. Think of some feature that your users may want to delagate to other users. Any feature can be broken down into a series of simple lists.

The first step, generally, would be to apply DCoSL to just one list. You, the developer, will create a default list, your own best guess as to what items should be on that list. Often, this may be a list that you, the developer, agoinze over, because you know that different users may have different ideas about what itms; belong on the list. So you give each user these options: use the default list; manage the list manually; or farm the list out to the WoT, using DIP-0 and perhaps other DIPs. If you are using DIP-0 by itself, you will write a bespoke method for list curation, typically using scraped data, e.g. a list of nostr relays scraped from the following list. Perhaps you agonize whether to expand one, two, three hops out? This decision can be farmed out to your user communities, using ideas from the DCoSL protocol.

The magic will become evident once additional, carefully chosen lists are added. Milestones can be created, defined by the things that your users can delegate. You may want to expand the simple list into a complex one, following DIPs below. Or you may wish to curate data models

Begin with the desired destination and then work backwars. That means: create a list of lists that together serve some function. Potentially, you will want to pick just one of the lists to offer for initial rollout to your users. Devise a method to curate that list. Provide an interface so that users have the following options: use the default list, curated by you, the team of developers; the user manages the list directly; or the users allows the web of trust to manage the list. Some intermediate states may be considered; for example, the WoT suggests updates to the list, which must then be approved manually, either individually or in aggregate, by the user. Once this is in place, then allow additional lists to be managed by DCoSL.

see examples 

# Protocol specification 

DIPs (DCoSL implementation proposals) are categorized into three blocks: the core protocol, the concept graph, and the grapevine.

## [DCoSL Core Protocol: DIPs 00 - 99](https://github.com/wds4/DCoSL/tree/main/dips)

The most important DIPs are DIP-00 and DIP-01. The only required DIP is DIP-00.

### DIP-00: Each list is in the eye of the beholder.

There is no universal list; each user it at the center of his or her web of trust, and each user's lists are curated independently.

### DIP-01: explicit, intentional attestations rather than scraped data

## [the concept graph: DIPs 100-199](https://github.com/wds4/DCoSL/tree/main/dips/conceptGraph)

From simple lists, to complex lists, to concepts, to the concept graph

threads, class threads, class node, class instance; analogy to the class in object-oriented programming

nodes, edges (relationships)
basic types of nodes: JSONSchema, wordType, set, superset, instance
basic types of relationships: subsetOf, JSONSchemaFor, specificInstanceOf
the Loki Principle = class thread rule

thread; class thread; class thread rule (principle of Loki)

three basic relationships between concepts

## [the grapevine: DIPs 200-299](https://github.com/wds4/DCoSL/tree/main/dips/grapevine)

weighted averages; contextual influence; each attestation is accompanied by confidence; each calculated score is accompanied by input, which is sum of weights

core relationships: attestations, ratings, endorsements

Entire libraries, platforms, protocols are subjected to decentralized curation via DCoSL. Repository management by dev teams, standards managed by committees, etc will diminish, because the option of management via WoT will exist.

Several of the proposed DIPs consist of lists: the list of node types, the list of relationships types, etc. In this series of DIPs, those lists are themselves curated according to the principles of DIP-0 and potentially other DIPs. 

## DIP infinity, aka Circular DCoSL

The DCoSL protocol is used to curate itself. Also referred to as `Circular DCoSL`, a phrase that pays homage to the 'circular economy' of bitcoin.

