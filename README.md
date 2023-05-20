# DCoSL: Decentralized Curation of Simple Lists
(alternate name: WeCoSL - Web-enabled Curation of Simple Lists; GCoSL, GdCoSL - Grapevine-directed Curation of Simple Lists; WIPs or GIPs instead of DIPs)

DCoSL is a simple, flexible protocol to guide construction of the decentralized web, decentralized reputation and web of trust. It is based on the premise that the ability for a user to delegate curation of a simple list to the web of trust (DIP-0) is the <i>atomic unit</i> and the <i>defining feature</i> of the decentralized web. Many attempts at web of trust have been tried, but have failed to gain traction. DCoSL strives to turn this into a tractable problem by breaking it down into bite size steps, by allowing your web of trust to curate one simple list at a time, and to curate only those lists that need to be farmed out to others.

In the spirit of nostr, dcosl is defined by a series of DIPs: dcosl implementation proposals. The first is mandadory, the rest are optional, and can be rolled out incrementally. In the final implementation, management of DCoSL has itself been handed over to your web of trust.

# Basic idea

The basic idea of DCoSL is to provide tools to allow users to farm out decisions, major and minor, to their webs of trust, thereby decreasing reliance on dev teams, standards committees, etc. This is handled through curation of simple lists: an unordered set of elements, referred to here as `items`. Examples of simple lists: a list of nostr relays, a list of trusted lightning nodes, a list of properties for a user profile (name, display_name, picture_url, etc).

DCoSL relies heavily on graphs. Why? Because a graph can be specified in full using two simple lists: one list for nodes, and one list for edges. A data model (e.g. a verifiable credential), an ontology, a schema or a context tree: these can all be built out of simple lists, each one of which can be curated. 

Alice's WoT and Bob's WoT, though they are not identical, are very likely to have significant overlap. For any given list, although there is no guarantee, there is a good chance that Alice and Bob will end up using the exact same (or at least almost the same) list! This is a vitally important attribute, one that I call loose consensus. You'll want to think deeply about loose consensus before incorporating decentralized list curation to your app.

If the contents of a list are not particularly polarizing or controversial (and most of them aren't), then there is a good chance that Alice's WoT and Bob's WoT will come up with the same, or at least very similar, lists. This is known as <i>loose consensus</i>. The power of DCoSL is its ability to generate loose consensus.

From a practical perspective, the challenge to the developer becomes which lists to curate and in what order to rollout list curation. Further broken down into manageable chunks by breaking the steps up into DIPs. The impact of DCoSL may not be apparent after curation of just one list. But as more lists are added, and more DIPs are adopted, the impact and significance will grow significantly.

The only proposal that is absolutely required for DCoSL is DIP-0. Every proposal after that is optional. For many proposals, specific details of implementation will be provided. DCoSL is designed to be tolerant of alternative implementations. Any implementation of a DIP that achieves the same purpose but differs only in details will be referred to as a `DIP-xx-substitute` or a `DIP-xx-equivalent`. (Provide example of this.) The final DIP, DIP-infinity, indicates that the implementation details of all previous DIPs are themselves curated using the DCoSL method. 

# Why do we need this?

Consider all of the awesome things we can do on the internet today that we could not do just a few short decades ago. All the highly sophisticated ways that two human beings, on opposite sides of the planet, can find each other like needles in a haystack, connect and interact, peer to peer. We have data curation (google search), eCommerce (Amazon, eBay), social media (Twitter, Facebook, Instgram), and more. Unfortunately, despite their peer to peer nature, these interactions are routed through increasingly large, centralized, powerful entities -- public and private -- that gain and more power and control over individuals and society at large. The goal of the decentralized web is to render these centralizing entities unnecessary. To provide the tools to reproduce these p2p interactions, and more. We will know we have succeeded when we no longer rely so heavily on platforms like those mentioned.

# How does DCoSL work?

The basic premise of DCoSL is that the ability for a user to delegate curation of a simple list to the web of trust (DIP-0) should be considered the <i>defining feature</i> of the decentralized web. If a platform does not satisfy NIP-0, it is not part of the decentralized web. If it does satisfy NIP-0, then it should be considered as part of the decentralized web, even if only one single list qualifies.

The reason that DCoSL will succeed where previous attempts at webs of trust have fallen short is that DCoSL offers a strategy to take a complex, overwhelming problem and break it down into small steps. How? As developers, you can provide your users with the ability to delegate list curation to their webs of trust in bite sized chunks: <i>one list at a time</i> (or perhaps a small handful of lists at a time).

## Everything can be broken down into lists

Several categories of lists, with examples, may be considered. See examples in this repo (work in progress).

A data model (e.g. a verifiable credential), an ontology, a schema or a context tree: these can all be built out of simple lists, each one of which can be curated. Imagine if your users no longer had to rely upon the World Wide Web Consortium (W3C) to manage a standard. With DCoSL, your users can farm out curation of any standard in question to their web of trust. Updates can potentially occur 24/7/365, not whenever the committee meets.

# Who should implement this? How to get started?

Any developer working on any peer to peer platform, protocol, library, or tool. Think of some feature that your users may want to delagate to other users. Any feature can be broken down into a series of simple lists.

The first step, generally, would be to apply DCoSL to just one list. The magic will become evident once additional, carefully chosen lists are added. Milestones can be created, defined by the things that your users can delegate. You may want to expand the simple list into a complex one, following DIPs below. Or you may wish to curate data models

Begin with the desired destination and then work backwars. That means: create a list of lists that together serve some function. Potentially, you will want to pick just one of the lists to offer for initial rollout to your users. Devise a method to curate that list. Provide an interface so that users have the following options: use the default list, curated by you, the team of developers; the user manages the list directly; or the users allows the web of trust to manage the list. Some intermediate states may be considered; for example, the WoT suggests updates to the list, which must then be approved manually, either individually or in aggregate, by the user. Once this is in place, then allow additional lists to be managed by DCoSL.

# Overview of the dcosl (wdcosl?) implementation proposals

## DIPs (WIPs?) 00 - ?: Fundamentals

### DIP-00: each user occupies the center of his or her web of trust (the Principle of Relativity)

use of graphs to represent data structures; use of cryptographic identifiers for nodes (and edges)

### DIP-01: explicit, intentional attestations rather than scraped data (the grapevine)

specifics: two types of ratings: endorse user as curator; endorse item

### DIP-02: complex lists

parent list augmented by auxiliary lists

### DIP-03: the Context tree and inheritance of average scores

## DIPs (GIPs?) ?-?: the grapevine

weighted averages; contextual influence; each attestation is accompanied by confidence; each calculated score is accompanied by input, which is sum of weights

core relationships

## DIPs (CIPs) ?-?: Concepts

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

