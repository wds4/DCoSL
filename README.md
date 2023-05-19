# DCoSL: Decentralized Curation of Simple Lists

DCoSL strives to be the most simple protocol imaginable for decentralized reputation and web of trust. In the spirit of nostr, dcosl is defined by a series of DIPs: dcosl implementation proposals. 

A simple list is an unordered set of elements, referred to here as `items`. An item is either an item on the list or it is not. Everything can be broken down into lists: a list of nostr relays, a list of trusted lightning nodes, a list of properties for a user profile (name, display_name, picture_url, etc). The basic premise of DCoSL is that the ability for a user to delegate curation of a simple list to the web of trust (DIP-0) is the <i>atomic unit</i> and the <i>defining feature</i> of the decentralized web.

# Basic idea

Many attempts at web of trust have been tried, but have failed to gain traction. DCoSL strives to turn this into a tractable problem by breaking it down into bite size steps, by allowing your web of trust to curate one simple list at a time. From a practical perspective, the challenge to the developer becomes which lists to curate and in what order to rollout list curation. Further broken down into manageable chunks by breaking the steps up into DIPs. The impact of DCoSL may not be apparent after curation of just one list. But as more lists are added, and more DIPs are adopted, the impact and significance will grow significantly.

The only proposal that is absolutely required for DCoSL is DIP-0. Every proposal after that is optional. For many proposals, specific details of implementation will be provided. DCoSL is designed to be tolerant of alternative implementations. Any implementation of a DIP that achieves the same purpose but differs only in details will be referred to as a `DIP-xx-substitute` or a `DIP-xx-equivalent`. (Provide example of this.) The final DIP, DIP-infinity, indicates that the implementation details of all previous DIPs are themselves curated using the DCoSL method. 

# Why do we need this?

Consider all of the awesome things we can do on the internet today that we could not do just a few short decades ago. All the highly sophisticated ways that two human beings, on opposite sides of the planet, can find each other like needles in a haystack, connect and interact, peer to peer. We have google search, eCommerce, social media, and more. Unfortunately, despite their peer to peer nature, these interactions are routed through increasingly large, centralized, powerful entities -- public and private -- that gain and more power and control as a result. The goal of the decentralized web is to render these centralizing entities unnecessary. To provide the tools to reproduce these p2p interactions, and more. The fact that we still use them is how we know we have not yet succeeded.

# How does DCoSL work?

The basic premise of DCoSL is that the ability for a user to delegate curation of a simple list to the web of trust (DIP-0) should be considered the <i>defining feature</i> of the decentralized web. If a platform does not satisfy NIP-0, it is not part of the decentralized web. If it does satisfy NIP-0, then it should be considered as part of the decentralized web, even if only one single list qualifies.

The reason that DCoSL will succeed where previous attempts at webs of trust have fallen short is that DCoSL offers a strategy to take a complex, overwhelming problem and break it down into small steps. How? As developers, you can provide your users with the ability to delegate list curation to their webs of trust in bite sized chunks: <i>one list at a time</i> (or perhaps a small handful of lists at a time).

## Loose consensus

If the contents of a list are not particularly polarizing or controversial (and most of them aren't), then there is a good chance that Alice's WoT and Bob's WoT will come up with the same, or at least very similar, lists. This is known as <i>loose consensus</i>. The power of DCoSL is its ability to generate loose consensus.

## Everything can be broken down into lists

Several categories of lists, with examples, may be considered. See examples in this repo (work in progress).

A data model (e.g. a verifiable credential), an ontology, a schema or a context tree: these can all be built out of simple lists, each one of which can be curated. Imagine if your users no longer had to rely upon the World Wide Web Consortium (W3C) to manage a standard. With DCoSL, your users can farm out curation of any standard in question to their web of trust. Updates can potentially occur 24/7/365, not whenever the committee meets.

# Who should implement this? How to get started?

Any developer working on any peer to peer platform, protocol, library, or tool. Think of some feature that your users may want to delagate to other users. Any feature can be broken down into a series of simple lists.

The first step, generally, would be to apply DCoSL to just one list. The magic will become evident once additional, carefully chosen lists are added. Milestones can be created, defined by the things that your users can delegate. You may want to expand the simple list into a complex one, following DIPs below. Or you may wish to curate data models

Begin with the desired destination and then work backwars. That means: create a list of lists that together serve some function. Potentially, you will want to pick just one of the lists to offer for initial rollout to your users. Devise a method to curate that list. Provide an interface so that users have the following options: use the default list, curated by you, the team of developers; the user manages the list directly; or the users allows the web of trust to manage the list. Some intermediate states may be considered; for example, the WoT suggests updates to the list, which must then be approved manually, either individually or in aggregate, by the user. Once this is in place, then allow additional lists to be managed by DCoSL.

# Overview of the dcosl implementation proposals

# DIPs 0 - ?: Fundamentals

## DIP-0: the core protocol

### Simple Lists

A simple list is exactly what it sounds like. An unordered set of items. Any given item is either on the list or it isn't. Each list and each item of each list has no more than a handful of properties. In Pretty Good Apps, each list has a name (with a singular and a plural form) and a description, all of which are strings. Each item has a name and a description, nothing more.

Any user can sumit a new list. Any user can submit a new item to any list.

Additional structure, such as an ordering to the list, partitioning into subsets, additional properties for list items, etc, are allowed but are not necessary to satisfy this dip. How to add some of these structures to a list (using additional, auxiliary simple lists) are addressed in later dips.

### Decentralized Curation

The particulars of the web of trust, the method of curation are not relevant to this nip. The only requirements are that each user is at the center of his or her own web of trust, and that the [Principle of Relativity for the Web of Trust](https://github.com/wds4/rebooting-the-web-of-trust/blob/master/Principle-of-Relativity-for-WoT.md) must be observed and respected. There is no Universal List. Each and every user maintains his or her own list. Alice's list and Bob's list may or may not be the same.

## DIP-1: The grapevine: explicit, intentional attestations rather than scraped data

In DCoSL, the term: `grapevine` is used informally in place of `web of trust` to refer to a web of trust that is built out of intentional attestations rather than scraped data. In addition, as many note, the word `trust` is frequently misleeading and inaccurate for the purpose at hand.

According to this dip, list curation is based upon explicit attestations (EA) rather than scraped data (SD) obtained using other methods. These are two opposing methods for list curation, described and discussed (here). An example of an explicit attestation would be the signed statement: Alice endorses [array of pubkeys ] as sources of trustworthy content. An example of scraped data would be a WoT built upon a following list. 

DIP-1 is based on the attitude that curation via EA is more trustworthy than SD, and that the superiority of EA will grow as the DCoSL ecosystem grows and matures. Of course, a combination of these two methods may be utilized. This dip details a method to use EA by itself.

## DIP-2: Score calculation

## DIPs ?-?: grow a simple list into a complex list, and ultimately into a 'concept'

## DIPs ?-?: relationships between lists: the concept graph

## DIPs ?-?: data models as graphs, a graph as a small handful of lists

## DIP infinity

Entire libraries, platforms, protocols are subjected to decentralized curation via DCoSL. Repository management by dev teams, standards managed by committees, etc will diminish, because the option of management via WoT will exist.

## DIPs ?-?: the web of trust

## DIPs ?-?: the circular economy; the diminishment of the managed repository

Several of the proposed DIPs consist of lists: the list of node types, the list of relationships types, etc. In this series of DIPs, those lists are themselves curated according to the principles of DIP-0 and potentially other DIPs. 

The design decisions outlined above can ultimately themselves be decomposed into simple lists and subjected to decentralized curation. 

