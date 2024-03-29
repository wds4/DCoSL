# DCoSL: Decentralized Curation of Simple Lists

*As of Feb 2024, this repo is being moved and rewritten as the [tapestry protocol](https://github.com/wds4/tapestry-protocol/blob/main/README.md)*

## Preamble

This repo is a work in progress. It is being implemented in the desktop app, [Pretty Good Apps](https://github.com/wds4/pretty-good), which is also a work in progress. If you want an example from my app to illustrate what I mean when I talk about using your web of trust to curate a list, follow [this link](https://github.com/wds4/pretty-good/blob/main/appDescriptions/curatedLists/exampleListCuration.md).

## Intro

DCoSL is a flexible protocol to guide the step-by-step construction of a decentralized web, with an emphasis on decentralized reputation and web of trust. Its design is inspired by the [nostr protocol](https://github.com/nostr-protocol/nostr). The protocol that follows is written to sit atop of nostr but could also be implemented in a nostr-independent fashion with minimal changes to the DCoSL protocol as currently specified.

The DCoSL protocol is based on the premise that the curation of a [simple list](glossary/simpleList.md) by one's web of trust should be considered not only the atomic unit of the decentralized web, but also its defining feature. DCoSL strives to turn a difficult and perhaps seemingly overwhelming challenge -- creation of a web of trust that lots of people actually use -- into a tractable one by breaking it down into bite size steps: one list at a time, and one [DIP (DCoSL implementation proposal)](dips) at a time.

Just about anything can be expressed in terms of lists: a list of trusted lightning nodes, a list of nostr relays, a list of user properties (display_name, about, picture_url, etc), a list of nodes & a list of edges in a [graph database](glossary/graphDatabase.md), and so on. Multiple lists used together can result in a [complex list](glossary/complexList.md), with 'complex' referring to the fact that the list is imbued with special features like subsets, customized properties for items on the list, etc. Out of simple lists, data structures, protocols, etc can be constructed that are as basic or as sophisticated as they need to be. And with DCoSL, those can be managed in a truly decentralized fashion.

With DCoSL, developers build tools to allow users to farm out various decisions, whether large or small, to communities of users. By choosing a list or lists carefully, a magical thing can emerge called [loose consensus](glossary/looseConsensus.md): under the right circumstances, especially for lists that are not controversial, Alice's WoT and Bob's WoT, though they may not be identical, could very easily have significant overlap, and could very easily end up farming out the curation of said list(s) to the same small group of trusted list curators (who may simply be the only people with the time and inclination to curate this particular list!). Although not enforced or guaranteed (hence the term: 'loose'), for a large category of lists, Alice and Bob will end up using the exact same (or at least almost the same) list! Shared lists, shared protocols, shared data structures, shared language; these obviate the need for any centralized entity to build and maintain a platform.

The term [crowdsourcing](glossary/crowdsource.md) will be used to refer to curation of one or a group of simple lists where a high degree of loose consensus is expected. [Schemas](https://schema.org/docs/schemas.html), data models, [verifiable credentials](https://www.w3.org/TR/vc-data-model/) and other [standards and specifications](https://www.w3.org/standards/), etc can be crowdsourced.

In the spirit of nostr, DCoSL is defined by a series of DIPs: DCoSL implementation proposals. Like nostr, a small handful of core DIPs go a long way. Most of the rest can be rolled out incrementally. Likewise, lists can be farmed out incrementally, allowing more and more design decisions to be placed under the control of user communities. In the long run, <i>even the management of the DCoSL protocol itself can be farmed out using the DCoSL protocol</i>, a state called `NIP-infinity` or `circular DCoSL` (this name paying homage to the notion of the 'circular economy').

# Why do we need DCoSL?

If the goal of Bitcoin is to decentralize the flow of value, it may be said that the goal of the decentralized web is to decentralize the flow of information. This is the motivation of DCoSL as well as nostr.

What is our vision for the decentralized web? We live on a planet with billions of people, free (one would hope) to associate and interact as they wish. What does that mean? It means: the spontaneous, dynamic organization of individuals into networks both large and small, sometimes overlapping, each one of which is capable of highly sophisticated intra-network communication and coordinated action. As cypherpunks we strive to build the tools to serve those needs. Tools that can be customized to the specific, changing, frequently unforseen (by devs) needs of each network. But there's a catch: we strive to build tools that <i>do not require any one person, developer, team, or entity to manage those tools or to be in charge of the network</i>. Have we succeeded? We're making progress, but we're not there yet.

Consider all of the awesome things we can do on the internet today that we could not do just a few short decades ago. All the highly sophisticated ways that two human beings, on opposite sides of the planet, can find each other like needles in a haystack, connect and interact, peer to peer. We have data curation (Google search), eCommerce (Amazon, eBay), social media (Twitter, Facebook, Instgram), and more. Unfortunately, despite their peer to peer nature, these interactions are routed through increasingly large, centralized, powerful entities -- public and private -- that gain more and more power and control over individuals and society at large, to the detriment of us all. These centralized entities provide the shared consensus required for sophisticated, specialized peer to peer interactions. But these centralized entities are always in charge of the networks which form around them. They create the platforms, the shared languages. They have the power. The goal of the decentralized web is to render these centralizing entities unnecessary.

Open source software is a marked improvement over proprietary software, but is not a perfect answer to the above problems. Developers who manage repositories, committees that manage standards, continue to exercise control that is not always fully mitigated despite the benefits of open source such as the ability to fork projects which most users have neither the time, expertise, or motivation to carry out. One of the goals of DCoSL is to give users the option to farm out ("[crowdsource](glossary/crowdsource.md)") management of standards, libraries, protocols, etc to a decentralized web of trust, to give that option to users who don't necessarily know how to code, and to make that option as easy as clicking a button. 

As long as we continue to need today's centralized tech platforms, as long as we continue to need the various standards bodies frequently associated with them, we should know that we have not yet succeeded.

# Why will DCoSL succeed where others have failed?

People have been trying to build webs of trust going back at least as far as 1991 when Phil Zimmerman released Pretty Good Privacy. Unfortunately, none have seemed to gain the sort of traction that was initially expected and desired. 

DCoSL strives to draw lessons from the success of bitcoin and nostr, each of which created or accomplished something previously thought by many to be impossible, or at least infeasible. Neither bitcoin nor nostr were the product of some shiny new technology. Each uses tools that had been laying around for quite some time. Simplicity of the starting point. The bitcoin consensus rules have no extraneous details. The nostr core protocol is as stripped down as can be. I think lightning is cool; but the consensus rules, to their credit, do not obligate the use of lightning. You may think kademlia is cool, or some decentralized identifier (DID) implementation is particularly cool, and you may be right. But nostr, to its credit, does not obligate the developer or the user to commit to these or to much else. Most NIPs are optional. 

The DCoSL protocol is designed in the same way. No matter how awesome are any of the DIPs beyond the first few, they are optional. In many cases, for many DIPs, there may be multiple similar but not necessarily identical ways to achieve the same goal ('DIP-xx-equivalents'). DCoSL does not require interacting users to implement the same DIPs, or to implement them in the same way. This is part of loose consensus: on any given list, consensus is highly likely to happen, but if it doesn't happen or if it's not perfect, that's OK. Lack of consensus on some minor detail will not require Alice and Bob to segregate into two nonoverlapping, noninteracting, completely separated networks (which is what typically happens if some open source platform gets forked).

Edit - add somewhere to this section: To use nostr, all you need to get started is NIP-1. (Need to check whether this is accurate.) As a starting point, NIP-1 is simplicity itself, compared to, say, the vast suite of libraries necessary just to get started on Bluesky. Likewise, the bitcoin consensus rules are as lean as can be. This cannot be said for the vast majority of alts. The lesson? Figure out the starting point and distill it to its essence. Strip away all that is superfluous. DCoSL takes this lesson from bitcoin and from nostr. This is why DCoSL will succeed where all other WoT attempts have falied.

# Why has DCoSL not been done before?

DCoSL requires an understanding and appreciation of several key concepts (below), most notably loose consensus and DIP-infinity (aka circular DCoSL) and a belief that such things are both possible and desirable. It can be challenging to build up or to convey any one of these concepts without the other concepts already in place.

In addition, DCoSL requires a clear starting point and a roadmap. DIP-00 is an easy starting point for any project. DIP-01 is a more difficult hurdle: it is relatively easy to describe but requires considerably more work for the developer to implement. Subsequent DIPs provide the building blocks of a roadmap. Although the benefits of early stage DIPs may be slight, the potential benefits of additional DIPs and a maturing DCoSL ecosystem are enormous. But no developer would ever start building these tools and following this roadmap without some assurance that the big picture is a sensible one. Hopefully, this document will be able to convey this roadmap along with its big picture including its endpoint, DIP-infinity.

In addition to the above, some may have philosophic difficulties with the starting point, DIP-00 (for any curated list, there is no universal, 'correct' master list), analogous to the philosophic difficulties of the number zero of some societies in ages past. So some maybe gotta get past that.

# Important concepts

## Everything can be broken down into [simple lists](glossary/simpleList.md)

## The power of DCoSL comes from generation of [loose consensus](glossary/looseConsensus.md)

## [DIP-infinity](dips/coreProtocol/infinity.md): a state such that the implementation of DCoSL is itself crowdsourced using DCoSL.

This repo may still exist but it will be redundant, because your grapevine will manage your DIPs and everything else in this repo. Not only this repo, but other repos, standards committees, etc.

# Protocol specification 

See [DIPs](dips)

# Notes

DCoSL is a work in progress. I am basically starting with a vision for the desired end-state of a completely decentralized web (["DIP-infinity"](dips/coreProtocol/infinity.md)) and working backwards from there to where we are now. As of May 2023 I have the outline of a path and am working on filling in the details as much as possible. I am also very close to drawing a path from the current state of nostr (e.g. [NIP-51](https://github.com/nostr-protocol/nips/blob/master/51.md): Lists) to potential entry points into DCoSL. The flexibility of the DCoSL approach means that once the path from nostr to DCoSL is complete, other onboarding pathways (not necessarily nostr-related) should be possible as well.

Considering changing DCoSL to WeCoSL: Web-enabled Curation of Simple Lists, changing DIPs to WIPs, and changing my profile pic to Devo ;-)

