Refactor the desktop app, Curated Lists, as a web app: Phase 1
=====

## Overview

Curated Lists currently exists as a functioning app in the [Pretty Good Apps nostr desktop client](https://github.com/wds4/pretty-good). This [phase 1 bounty](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1.md) will be the first in a series of bounties to refactor this app as a web app with an improved design and user experience.

The requirements of phase 1 are simply to create an explorer for all kind: 9901 and 39901 events (proposed lists, list items, and the attestations used to curate which proposed items should be accepted vs rejected onto any given list by a reference user's web of trust) and should be relatively straightforward for an experienced dev. The actual curation itself (based on an analysis of the relevant attestations) is not necessary for Phase 1.

## Bounties: 
- [Phase 1](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1/phase1.md): 20,000,000 sats (+ up to 3,000,000 sats in bonuses - see below)
- [additional phases](https://github.com/wds4/DCoSL/tree/main/bounties/curatedLists): to be determined, pending the successful completion of phase 1

## Background

Curated Lists, one of the apps in the [Pretty Good Apps nostr desktop client](https://github.com/wds4/pretty-good), is a basic proof of concept implementation of the protocol for [DCoSL: Decentralized Curation of Simple Lists](https://github.com/wds4/dcosl).

The ultimate goal of DCoSL is to establish a roadmap to build tools for users to crowdsource knowledge by delegating the curation of information in a context-sensitive manner to one's web of trust. To do this well is a complex problem, but one that I have put a lot of thought into over the years, resulting in a roadmap that is sufficiently detailed that I believe makes it ready for implementation. The purpose of building this webapp is to generate feedback and discussion of some of the ideas and principles that underly this roadmap by putting them into production.

In its current form, Curated Lists is functional but needs significantly improved UX to attract users and gain visibility. I will be rolling out a series of bounties to refactor the existing functionality of Curated Lists as a website with an improved user experience (and maybe eventually to add some additional functionality, such as an API).

Phase 1 will not be a full implementation of curated lists, but will simply allow visitors to the site to explore existing lists, list items, endorsements of list items, and endorsements of users as list curators, all of which can currently be submitted as nostr events using the Pretty Good Apps nostr desktop client. Future phases will add more functionality, including the ability to submit new lists, list items, and attestations. The actual curation itself (designation of submitted items as `accepted` or `rejected` items on the list by the reference user's web of trust) will be a more complicated endeavor and will not be required to collect the Phase 1 bounty (but will probably be the core of one of the upcoming phases).

## Why DCoSL?

A graph is a versatile mathematical object that can be used to format and represent just about any type of data. Any individual graph can be specified in full using nothing more than two simple lists: one list for nodes and one list for edges. If we can figure a way to crowdsource a simple list *in a genuinely decentralized fashion*, then we can crowdsource a graph. And if we can crowdsource a graph, we can crowdsource just about any piece of data, including the symbols used in the representation of that data. If we can curate simple lists, we can curate the very tools that we use for communication.

The trick, then, is to curate simple lists in a manner that is worthy of the *decentralized* moniker.

## What I'm looking for

I'm looking for an individual (or a team) who is adept at web apps and **most importantly: excellent at design and UX**. Ideally you'll be interested in subsequent phases, but obviously there's no need to commit to that upfront.

Phase 1 should be relatively straightforward to implement for an experienced nostr developer with good design skllls. To make it easy for you to bang this out quickly, see this [overview](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1/pgaFunctionality.md) of how lists, list items, and attestations are currently formatted in the Curated Lists app. If you're an experienced dev but new to nostr and looking to learn, this could be a good way to become familiar with nostr while stacking a few sats!

I'd prefer this and subsequent phases to be built using the tools that I used for Pretty Good Apps -- most notably react -- but let me know if you'd like to use alternative tools and we can talk. I will certainly be open to suggestions!

Good design will be required for the full bounty. I'd be happy to consider selecting one or a few members of the nostr community to judge when the bounty has been met.

If phase 1 goes well, there will be many more phases to come!

## Pretty Good Apps functionality relevant to Phase 1

Follow [this link](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1/pgaFunctionality.md) to see how lists, list items, and attestations are formatted and stored in nostr. These will be the core of the data displayed in Phase 1. They can be downloaded by filtering for kinds 9901 (lists and list items) and 39901 (attestations).

## Details of the expected user experience

Follow [this link](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1/userExperience.md) for the expected user experience.

## Repo

Two options:
- you create your own repo, run your own website. Bounty paid once site fully functional.
- For additional 2,000,000 sats bonus: Build on one of my repositories (with AGPL-3.0) and I will host the website (perhaps on dcosl.com). Bounty (including bonus) paid once PR is accepted.

## Bonuses

### Bonus 1: repo; + 2 mil sats

(see section on Repo, above)

### Bonus 2: additional detail for nostr nerds; + 1 mil sats

Make it so that users who are devs can click a button and see the raw json data for `words` (formatted as per DCoSL) and `events` (words wrapped as nostr events). Purpose: make it easier for other devs to get up to speed. Only do this if you can figure out how to do it without detracting from the overall UX. See how I currently do this in Pretty Good Apps for reference.

## More info

Please DM me npub1u5njm6g5h5cpw4wy8xugu62e5s7f6fnysv0sj0z3a8rengt2zqhsxrldq3 with questions, ideas, or words of encouragement! :-)

Links:
- [DCoSL: Decentralized Curation of Simple Lists](https://github.com/wds4/DCoSL) protocol repository on github
- [Pretty Good Apps](https://github.com/wds4/pretty-good) repository on github
- [details of Phase 1](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1.md)
- the [overview](https://github.com/wds4/DCoSL/tree/main/bounties) of DCoSL and Pretty Good Apps bounties (including a roadmap for future bounties beyond this one).
