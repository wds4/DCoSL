# DCoSL: Decentralized Curation of Simple Lists
(alternate name: WeCoSL - Web-enabled Curation of Simple Lists; GCoSL, GdCoSL - Grapevine-directed Curation of Simple Lists; WIPs or GIPs instead of DIPs)

DCoSL is a simple, flexible protocol to guide construction of the decentralized web, decentralized reputation and web of trust. 

The DCoSL protocol is based on the premise that the decentralized curation of a simple list is the <i>atomic unit</i> and the <i>defining feature</i> of the decentralized web. DCoSL strives to turn a difficult and often seemingly overwhelming challenge -- a web of trust that truly gains traction -- into a tractable one by breaking it down into bite size steps: one list at a time, and one DIP at a time. Just about anything can be expressed in terms of simple lists: a list of trusted lightning nodes, a list of nostr relays, a list of user properties (display_name, etc), and so on. Successive compounding of simple lists can result in complex lists (e.g. to segregate list items into subsets, with subsets being another simple list). Out of simple lists, data structures can be constructed that are as complex as they need to be.

With DCoSL, developers provide tools to allow users to farm out various decisions, whether large or small, to communities of users. By choosing a list or lists carefully, a magical thing will often emerge called loose consensus: Alice's WoT and Bob's WoT, though they are not identical, are very likely to have significant overlap, and will likely farm out the curation of said list to the same small group of trusted list curators. For any given list, although there is no guarantee, there is a good chance that Alice and Bob will end up using the exact same (or at least almost the same) list!

In the spirit of nostr, dcosl is defined by a series of DIPs: dcosl implementation proposals. The first is mandadory, the rest are optional, and can be rolled out incrementally. As more and more design decisions are farmed out to users, and as more and more NIPs are implemented, the responsibilities of repo management will diminish. In the long run, even the DCoSL protocol itself can be farmed out to user communities, a state called NIP-infinity or circular DCoSL (like circular economy).

# Why do we need DCoSL?

If the goal of Bitcoin is to decentralize the flow of value, it may be said that the goal of DCoSL (as well as nostr) are to decentralize the flow of information.

Consider all of the awesome things we can do on the internet today that we could not do just a few short decades ago. All the highly sophisticated ways that two human beings, on opposite sides of the planet, can find each other like needles in a haystack, connect and interact, peer to peer. We have data curation (google search), eCommerce (Amazon, eBay), social media (Twitter, Facebook, Instgram), and more. Unfortunately, despite their peer to peer nature, these interactions are routed through increasingly large, centralized, powerful entities -- public and private -- that gain and more power and control over individuals and society at large. The goal of the decentralized web is to render these centralizing entities unnecessary. To provide the tools to reproduce these p2p interactions, and more. We will know we have succeeded when we no longer rely so heavily on platforms like those mentioned.

Open source software is a marked improvement over proprietary software, but is not a perfect answer to the above problems. Developers who manage repositories, committees that manage standards, continue to exercise control that is not always fully mitigated despite the benefits of open source such as the ability to fork projects which most users have neither the time, expertise, or motivation to carry out. One of the goals of DCoSL is to give users the option to farm out management of standards, libraries, protocols, etc to a decentralized web of trust, to give that option to users who don't necessarily know how to code, and to make that option as easy as clicking a button. 

# Why will DCoSL succeed where others have failed?

People have been trying to build webs of trust going back at least as far as 1991 when Phil Zimmerman released Pretty Good Privacy. Unfortunately, none have seemed to gain the sort of traction that was initially expected and desired. 

DCoSL strives to draw lessons from the success of Bitcoin and nostr, each of which achieved goals that appeared by many to be unachievable. Neither Bitcoin nor nostr were the product of some shiny new technology. Each uses tools that had been laying around for quite some time. Simplicity of the starting point. The bitcoin consensus rules have no extraneous details. The nostr core protocol is as stripped down as can be. I think lightning is cool; but the consensus rules, to their credit, do not obligate the use of lightning. You may think kademlia is cool, or some DID is cool, and you may be right. But nostr, to its credit, does not obligate the developer or the user to commit to these or to much else. Most NIPs are optional. 

The DCoSL protocol is designed in the same way. No matter how awesome are any of the DIPs beyoind DIP-0, they are optional. In many cases, for many DIPs, there may be multiple alternative ways to achieve the same goal. DCoSL does not require interacting users to implement the same DIPs, or to implement them in the same way. This is part of loose consensus: on any given list, consensus is highly likely to happen, but if it doesn't happen or if it's not perfect, that's OK.

# Why has DCoSL not been done before?

DCoSL requires an understanding and appreciation of loose consensus and DIP-infinity and a belief that such things are both possible and desirable. In addition, DCoSL requires a clear starting point and a roadmap. DIP-0 is an easy starting point for any project. DIP-1 is relatively easy to describe but requires considerably more work for the developer to implement. Subsequent NIPs provide the building blocks of a roadmap. Although the benefits of early stage NIPs may be slight, the potential benefits of maturing DCoSL are enormous.

In addition to the above, some may have philosophic difficulties with the starting point, DIP-0, analogous to the philosophic difficulties of the number zero of some societies in ages past. Gotta get past that.

# Important concepts

## Everything can be broken down into simple lists

Consider the following examples of simple lists:
<li></li>
<li></li>

A data model (e.g. a verifiable credential), an ontology, a schema or a context tree: these can all be built out of simple lists, each one of which can be curated. Imagine if your users no longer had to rely upon the World Wide Web Consortium (W3C) to manage a standard. With DCoSL, your users can farm out curation of any standard in question to their web of trust. Updates can potentially occur 24/7/365, not whenever the committee meets.

Several categories of lists, with examples, may be considered. See examples in this repo (work in progress).

## Loose Consensus 

One of the most important concepts to understand when picking which lists to farm out. Alice's WoT and Bob's WoT, though they are not identical, are very likely to have significant overlap. For any given list, although there is no guarantee, there is a good chance that Alice and Bob will end up using the exact same (or at least almost the same) list! This is a vitally important attribute, one that I call loose consensus. You'll want to think deeply about loose consensus before incorporating decentralized list curation to your app.

If the contents of a list are not particularly polarizing or controversial (and most of them aren't), then there is a good chance that Alice's WoT and Bob's WoT will come up with the same, or at least very similar, lists. This is known as <i>loose consensus</i>. The power of DCoSL is its ability to generate loose consensus.

From a practical perspective, the challenge to the developer becomes which lists to curate and in what order to rollout list curation. Further broken down into manageable chunks by breaking the steps up into DIPs. The impact of DCoSL may not be apparent after curation of just one list. But as more lists are added, and more DIPs are adopted, the impact and significance will grow significantly.

## DIP-infinity

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

# Overview of the dcosl (wdcosl?) implementation proposals

The only proposal that is absolutely required for DCoSL is DIP-0. Every proposal after that is optional. For many proposals, specific details of implementation will be provided. DCoSL is designed to be tolerant of alternative implementations. Any implementation of a DIP that achieves the same purpose but differs only in details will be referred to as a `DIP-xx-substitute` or a `DIP-xx-equivalent`. (Provide example of this.) The final DIP, DIP-infinity, indicates that the implementation details of all previous DIPs are themselves curated using the DCoSL method. 

## DIPs (WIPs?) 00 - ?: Fundamentals

### DIP-00: each user occupies the center of his or her web of trust (the Principle of Relativity)

use of graphs to represent data structures; use of cryptographic identifiers for nodes (and edges)

### DIP-01: explicit, intentional attestations rather than scraped data (the grapevine)

specifics: two types of ratings: endorse user as curator; endorse item

### DIP-02: complex lists

parent list augmented by auxiliary lists
subsets, subset trees, properties, property trees

### DIP-03: use of graphs to represent complex lists and other data structures

### DIP-04: the Context tree and inheritance of average scores

## DIPs (GIPs?) ?-?: the grapevine

weighted averages; contextual influence; each attestation is accompanied by confidence; each calculated score is accompanied by input, which is sum of weights

core relationships

## DIPs (CIPs) ?-?: Concepts
From simple lists, to complex lists, to concepts, to the concept graph

threads, class threads, class node, class instance; analogy to the class in object-oriented programming

basic types of nodes: JSONSchema, wordType, set, superset, instance
basic types of relationships: subsetOf, JSONSchemaFor, specificInstanceOf
the Loki Principle

## DIPs ?-?: relationships between concepts: the concept graph

three basic relationships between concepts

## DIPs ?-?: data models as graphs, a graph as a small handful of lists

nodes, edges
thread; class thread; class thread rule (principle of Loki)

## DIP infinity

Entire libraries, platforms, protocols are subjected to decentralized curation via DCoSL. Repository management by dev teams, standards managed by committees, etc will diminish, because the option of management via WoT will exist.

## DIPs ?-?: the web of trust

## DIPs ?-?: the circular economy; the diminishment of the managed repository

Several of the proposed DIPs consist of lists: the list of node types, the list of relationships types, etc. In this series of DIPs, those lists are themselves curated according to the principles of DIP-0 and potentially other DIPs. 

The design decisions outlined above can ultimately themselves be decomposed into simple lists and subjected to decentralized curation. 

