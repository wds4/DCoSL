Phase 1: Curated Lists explorer
=====

## Overview

Duplicate the existing functionality of the Curated Lists desktop app (part of [Pretty Good Apps](https://github.com/wds4/pretty-good) nostr desktop client) as a web app. This will be broken down into multiple phases. Phase 1 will be a simple Lists explorer, to see what lists, list items, and attestations have been submitted to the network (via the PGA client), but without the full functionality of Curated Lists. The actual curation of the lists (determining which items are accepted or rejected by the reference user's web of trust) is more complex and will not be required to collect the Phase 1 bounty (but will probably be the core of Phase 2).

Needs to be great UX for the full bounty. Including with thought given to future dev of the site. We will pick someone to judge.

## Bounties: 
- [Phase 1](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1.md): 20,000,000 sats (+ up to 4,000,000 sats in bonuses; see below)
- [additional phases](https://github.com/wds4/DCoSL/tree/main/bounties/curatedLists): to be determined

## what I'm looking for

I'm looking for someone who is adept at web apps, react, and **most importantly: excellent at design and UX** (which are my weak points!)

Phase 1 should be relatively straightforward to implement for an experienced nostr developer with good UX skllls. For those newer to nostr, this project could be a chance to learn some nostr basics while stacking a few sats!

I have provided lots of detail. If you're an experienced nostr dev, you could probably whip this out pretty quickly. If you're an experienced dev but new to nostr and looking to learn, this could be a good way to become familiar while stacking a few sats!

## Background

Curated Lists, one of the apps in the [Pretty Good Apps](https://github.com/wds4/pretty-good) desktop nostr client, is an exploratory proof of concept implementation of the [DCoSL](https://github.com/wds4/dcosl) procotol, the ultimate goal of which is to build tools for users to crowdsource data by delegating the curation of information to one's web of trust. To do this well is a complex problem, but one that I have put a lot of thought into over the years.

In its current form, Curated Lists is functional but needs better UX to attract users and gain visibility. A series of bounties is envisioned to refactor the existing functionality of Curated Lists as a website (and maybe eventually to add some additional functionality, such as an API).

Rather than improve the UX of the existing desktop client (UX not being my strong suit), I would like to focus on fleshing out the repo for the DCoSL protocol itself, which is woefully incomplete. I would also like to author and submit a NIP that might act as a bridge between nostr and dcosl. For now, the best reference for the dcosl protocol is its implementation in the Pretty Good Apps desktop client.

## Functionality for Phase 1

The web app will download 4 types of events (Pretty Good Apps client makes it easy for you to see in detail how these events are formatted) 
- lists: kind: 9901, `s` tag: `nostrCuratedList`
- list items: kind 9901, `e` tag which corresponds to the event ID of the parent list
- endorsement of list item: kind 39901, `r` tag: `7e92c80fb7d3fa7bec453c8b3c6db306bdde50f7eee34e76a880fe0ab770d485-genericContext`
- endorsement of user as a curator of a given list: kind 39901, `r` tag: `7e92c80fb7d3fa7bec453c8b3c6db306bdde50f7eee34e76a880fe0ab770d485-nostrCuratedListsCuratorEndorsement-genericContext`

Filter for kinds: 9901 and 39901 will get all relevant events for Curated Lists. The rating itself is stored in the `ccontent` field and can be extracted as a json object, which contains information to determine what is being rated.

See [DIP-1104](https://github.com/wds4/DCoSL/blob/main/dips/networking/nostr/1104.md): publication of attestation over nostr

## User experience

UX is not my forte so I will be looking for someone with good design instincts.

Sign-in with a nostr key will not be required for Phase 1 (probably not until Phase 3).

Visitors to the site will be presented with two options:
- select an existing list 
- select a reference ("seed") user

### list selection

All valid lists should be selectable. 

For initial rollout, with only a small number of lists to choose from, a simple drop-down menu would suffice. But once the number of lists increases, it will likely be desirable to make lists searchable by list name, list decription, author, date of submission, list event ID, and number of items. 

Once phase 2 is implemented, several other curation-related parameters could also be useful for search (e.g. to select for lists depending on how many ratings from trusted users have been received).

Once a list is selected, the viewer should be able to see list details, including:
- list name
- list description
- list author, with concise author details (icon, name, etc)
- date of list submission
- optional: Bonus #2 list information

### seed user selection

After making selections for list and seed user, the site will display:
- basic list information, including list name, list description, the author of the list, and when it was created
- all items that have been submitted to that list, with the ability to view each item name, item description, author of the item, and date of submission

In addition, the viewer should be able to review all attestations relevant to the selected list. Attestations are submitted as kind: 39901 events. (Pretty Good Apps will make it easy for you to see how these events are formatted.) There are two types of attestations:
- endorse (or reject) an item as "belonging" or not belonging on the list to which it is submitted
- endorse (or reject) a user as being a trusted (or not) curator of that particular list

The options for seed user will consist of all users who have received attestations as Curators of that particulat list. In addition, the visitor should have the ability to add any arbitrary npub as seed user.

The above should have an easy to navigate UX. Notably, the actual curation of list items (segregation into accepted, rejected, and pending) does not need to be implemented until Phase 2. However, the UX of Phase 1 should be designed with Phase 2 in mind.

## Repo

Two options:
- you create your own repo, run your own website. Bounty paid once site fully functional.
- For additional 2,000,000 sats bonus: Build on one of my repositories (with AGPL-3.0) and I will host the website (perhaps on dcosl.com). Bounty (including bonus) paid once PR is accepted.

I'd be happy to designate a prearranged mutual acquaintance within the nostr community as arbiter to determine when bounty requirements have been met.

## Bonuese

### Bonues 1: repo; + 2 mil sats

(see above)

### Bonus 2: additional detail for nostr nerds; + 2 mil sats

Only if you can figure out how to do this without detracting from the overall UX. Make it so that users who are devs can explore the events and words. See pic of how I do this in Pretty Good Apps.

## More info

Please DM me npub1u5njm6g5h5cpw4wy8xugu62e5s7f6fnysv0sj0z3a8rengt2zqhsxrldq3 with questions, ideas, or words of encouragement! :-)

For updated info, see the [overview](https://github.com/wds4/DCoSL/tree/main/bounties) of DCoSL and Pretty Good Apps bounties (including a roadmap for future bounties beyond this one).
