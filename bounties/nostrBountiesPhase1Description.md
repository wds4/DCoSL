Refactor the desktop app, Curated Lists, as a web app
=====
Implement the [phase 1 bounty](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1.md) for curated lists. 
-----

Follow [this link](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1.md) for details.

## Overview

Currently Curated Lists exists as a functioning app in the [Pretty Good Apps nostr desktop client](https://github.com/wds4/pretty-good). This phase 1 bounty will be the first in a series of bounties to refactor this app as a web app with superior UX.

## Bounties: 
- [Phase 1](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1.md): 15,000,000 sats (+ up to 3,000,000 sats in bonuses; see below)
- [additional phases](https://github.com/wds4/DCoSL/tree/main/bounties/curatedLists): to be determined, pending the successful completion of phase 1

## Background

Curated Lists, one of the apps in the [Pretty Good Apps nostr desktop client](https://github.com/wds4/pretty-good), is a basic proof of concept implementation of the protocol for [DCoSL: Decentralized Curation of Simple Lists](https://github.com/wds4/dcosl).

The ultimate goal of DCoSL is to establish a roadmap to build tools for users to crowdsource knowledge by delegating the curation of information to one's web of trust. To do this well is a complex problem, but one that I have put a lot of thought into over the years, and I believe that I have a tractable roadmap. The purpose of building this webapp is to generate feedback and discussion of some of these ideas by putting them into production.

In its current form, Curated Lists is functional but needs significantly improved UX to attract users and gain visibility. I will be rolling out a series of bounties to refactor the existing functionality of Curated Lists as a website with a superior user experience (and maybe eventually to add some additional functionality, such as an API).

Phase 1 will not be a full implementation of curated lists, but will simply allow visitors to the site to explore existing lists, list items, endorsements of list items, and endorsements of users as list curators, all of which can currently be submitted as nostr events using the Pretty Good Apps nostr desktop client. Future phases will add more functionality, including the ability to submit new lists, list items, and attestations. The actual curation itself (designation of submitted items as `accepted` or `rejected` items on the list by the reference user's web of trust) will be a more complicated endeavor and will not be required to collect the Phase 1 bounty (but will probably be the core of Phase 2).

Needs to be great UX for the full bounty. Including with thought given to future dev of the site. We will pick someone to judge.

## Why DCoSL?

A graph is a versatile mathematical object that can be used to format and represent just about any type of data. Any individual graph can be specified in full using nothing more than two simple lists: one list for nodes and one list for edges. If we can figure a way to crowdsource a simple list in a genuinely decentralized fashion, then we can crowdsource a graph. And if we can crowdsource a graph, we can crowdsource just about any piece of data, including the symbols used in its representation.

## what I'm looking for

I'm looking for an individual (or a team) who is adept at web apps, react, and **most importantly: excellent at design and UX**.

Phase 1 should be relatively straightforward to implement for an experienced nostr developer with good design skllls. To make it easy for you to bang this out quickly, I provide relevant [details](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1.md). If you're an experienced dev but new to nostr and looking to learn, this could be a good way to become familiar with nostr while stacking a few sats!

If phase 1 goes well, there will be many more phases to come!

## More info

Please DM me npub1u5njm6g5h5cpw4wy8xugu62e5s7f6fnysv0sj0z3a8rengt2zqhsxrldq3 with questions, ideas, or words of encouragement! :-)

References:
- [DCoSL: Decentralized Curation of Simple Lists](https://github.com/wds4/DCoSL) repository on github
- [Pretty Good Apps](https://github.com/wds4/pretty-good) repository on github
- [details of Phase 1](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1.md)
- the [overview](https://github.com/wds4/DCoSL/tree/main/bounties) of DCoSL and Pretty Good Apps bounties (including a roadmap for future bounties beyond this one).
