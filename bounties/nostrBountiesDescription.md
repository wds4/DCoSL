# Refactor the desktop app, Curated Lists, as a web app

## Overview

Duplicate the existing functionality of the Curated Lists desktop app (part of [Pretty Good Apps](https://github.com/wds4/pretty-good) nostr desktop client) as a web app. This will be broken down into multiple phases. Phase 1 will be a simple Lists explorer, to see what lists and list items have been submitted to the network (currently can only do submissions using the PGA client), but without the full functionality of Curated Lists. The actual curation of the lists (determining which items are accepted or rejected by the reference user's web of trust) is more complex and will not be required to collect the Phase 1 bounty.

Phase 1 should be relatively straightforward to implement for an experienced nostr developer with good UX skllls. For those newer to nostr, this project could be a chance to learn some nostr basics while stacking a few sats!

## Bounties: 
- [Phase 1](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1.md): 10,000,000 sats (+ optional 2,000,000 sats bonus; see below)
- [additional phases](https://github.com/wds4/DCoSL/tree/main/bounties/curatedLists): to be determined

## Background

Curated Lists, one of the apps in the [Pretty Good Apps](https://github.com/wds4/pretty-good) desktop nostr client, is an exploratory proof of concept implementation of the [DCoSL](https://github.com/wds4/dcosl) procotol, the ultimate goal of which is to build tools for users to crowdsource data by delegating the curation of information to one's web of trust. This is a complex problem, but one that I have put a lot of thought into over the years.

In its current form, Curated Lists is functional but needs better UX to attract users and gain visibility. A series of bounties is envisioned to refactor the existing functionality of Curated Lists as a website (and maybe eventually to add some additional functionality, such as an API).

Rather than improve the UX of the existing desktop client (UX not being my strong suit), I would like to focus on fleshing out the repo for the DCoSL protocol itself, which is woefully incomplete. I would also like to author and submit a NIP that might act as a bridge between nostr and dcosl. For now, the best record of the dcosl protocol is its implementation in the Pretty Good Apps desktop client.

## Functionality for Phase 1

Sign-in with a nostr key will not be required for Phase 1 (probably not until Phase 3). Visitors to the site will be presented with two options:
- select an existing list
- select a "seed" user
  
Existing lists will be those that have been posted as kind: 9901 events using the DCoSL protocol. (Pretty Good Apps will make it easy for you to see how these events are formatted.) 

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

## More info

Please DM me npub1u5njm6g5h5cpw4wy8xugu62e5s7f6fnysv0sj0z3a8rengt2zqhsxrldq3 with questions, ideas, or words of encouragement! :-)

For updated info, see the [overview](https://github.com/wds4/DCoSL/tree/main/bounties) of DCoSL and Pretty Good Apps bounties (including a roadmap for future bounties beyond this one).
