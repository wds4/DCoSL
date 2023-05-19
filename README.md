# DCoSL: Decentralized Curation of Simple Lists

DCoSL strives to be the most simple protocol imaginable for decentralized reputation and web of trust. In the spirit of nostr, dcosl is defined by a series of DIPs: dcosl implementation proposals. The only proposal that is absolutely required is DIP-0. Every proposal after that is optional.

# Why do we need this?

Consider all of the awesome things we can do on the internet today that we could not do just a few short decades ago. All the highly sophisticated ways that two human beings, on opposite sides of the planet, can find each other like needles in a haystack, connect and interact, peer to peer. We have google search, eCommerce, social media, and more. Unfortunately, despite their peer to peer nature, these interactions are routed through increasingly large, centralized, powerful entities -- public and private -- that gain and more power and control as a result. The goal of the decentralized web is to render these centralizing entities unnecessary. To provide the tools to reproduce these p2p interactions, and more. The fact that we still use them is how we know we have not yet succeeded.

# How does DCoSL work?

The basic premise of DCoSL is that the ability for a user to delegate curation of a simple list to the web of trust (NIP-0) should be considered the <i>defining feature</i> of the decentralized web. If a platform does not satisfy NIP-0, it is not part of the decentralized web. If it does satisfy NIP-0, then it should be considered as part of the decentralized web, even if only one single list qualifies.

The reason that DCoSL will succeed where previous attempts at webs of trust have fallen short is that DCoSL offers a strategy to take a complex, overwhelming problem and break it down into small steps. How? As developers, you can provide your users with the ability to delegate list curation to their webs of trust in bite sized chunks: <i>one list at a time</i> (or perhaps a small handful of lists at a time).

## Loose consensus

If the contents of a list are not particularly polarizing or controversial (and most of them aren't), then there is a good chance that Alice's WoT and Bob's WoT will come up with the same, or at least very similar, lists. This is known as <i>loose consensus</i>. The power of DCoSL is its ability to generate loose consensus.

## Everythung can be broken down into lists

A data model (e.g. a verifiable credential), an ontology, a schema or a context tree: these can all be built out of simple lists, each one of which can be curated. Imagine if your users no longer had to rely upon the World Wide Web Consortium (W3C) to manage a standard. With DCoSL, your users can farm out curation of any standard in question to their web of trust. Updates can potentially occur 24/7/365, not whenever the committee meets.

# Who should implement this? How to get started?

Any developer working on any peer to peer platform, protocol, library, or tool. Think of some feature that your users may want to delagate to other users. Any feature can be broken down into a series of simple lists.

The first step, generally, would be to apply DCoSL to just one list. The magic will become evident once additional, carefully chosen lists are added. Milestones can be created, defined by the things that your users can delegate. You may want to expand the simple list into a complex one, following DIPs below. Or you may wish to curate data models

# Overview of the dcosl implementation proposals

## DIP-0: the core protocol

### Simple Lists

A simple list is exactly what it sounds like. An unordered set of items. Any given item is either on the list or it isn't. Each list and each item of each list has no more than a handful of properties. In Pretty Good Apps, each list has a name (with a singular and a plural form) and a description, all of which are strings. Each item has a name and a description, nothing more.

Any user can sumit a new list. Any user can submit a new item to any list.

Additional structure, such as an ordering to the list, partitioning into subsets, additional properties for list items, etc, are allowed but are not necessary to satisfy this dip. Some of these structures are addressed in later dips.

### Decentralized Curation

The particulars of the web of trust, the method of curation are not relevant to this nip. The only requirements are that each user is at the center of his or her own web of trust, and that the [Principle of Relativity for the Web of Trust](https://github.com/wds4/rebooting-the-web-of-trust/blob/master/Principle-of-Relativity-for-WoT.md) must be observed and respected. There is no Universal List. Each and every user maintains his or her own list. Alice's list and Bob's list may or may not be the same.

## DIPs 1-?: grow a simple list into a complex list, and ultimately into a 'concept'

## DIPs ?-?: relationships between lists: the concept graph

## DIPs ?-?: data models as graphs, a graph as a small handful of lists

## DIPs ?-?: the web of trust

## DIPs ?-?: the circular economy; the diminishment of the managed repository

The design decisions outlined above can ultimately themselves be decomposed into simple lists and subjected to decentralized curation. 

