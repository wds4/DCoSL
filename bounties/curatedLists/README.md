Refactor Curated Lists as a website with better UX
=====

## Background

Curated Lists, one of the apps in the Pretty Good Apps desktop nostr client, is a proof of concept implementation of the DCoSL procotol and arguably the first ever implementation of decentralized knowledge curation, as per the [core principles of DCoSL](../../dips/coreProtocol).

In its current form, Curated Lists is functional but needs better UX to attract users and gain visibility. The goal of this series of bounties is to refactor the existing functionality of Curated Lists as a website (and possibly to add some additional functionality, such as an API). 

Currently Phase 1 is the only bounty that has been finalized. Bounties for subsequent phases will be finalized upon the successful completion of Phase 1.

# [Phase 1: Curated Lists explorer](./phase1.md)

Create a website where users can browse existing Curated Lists and observe the results of list curation using different seed users. Compare to [listr.lol](https://listr.lol) (plus the list curation calculations, minus the log in).

## Bounty: 10,000,000 sats -- or make an offer!

# [Phase 2: User sign-in and data submission](./phase2.md)

Allow users to sign in to the website (using standard nostr tools such as getalby) to that they can:
- make new lists (kind: 9901)
- add items to existing lists (kind: 9901)
- endorse/reject items (kind: 39901)
- endorse/reject list curators (kind: 39901)

## Bounty: to be determined

# [Phase 3: add the grapevine Control Panel](./phase3.md)

There are a number of adjustable constants that are used when calculating. For Phase 1, default values will be used for all constants. For this phase, a control panel will be added which allows the user to adjust constants and observe the change in real time on list curation.

## Bounty: to be determined

# [Phase 4: visualization of the grapevine](./phase4.md)

Graphical representation of the web of trust with the ability to review the calculations of weighted averages for individual List Curators and List Items

## Bounty: to be determined

# [Phase 5: API](./phase5.md)

Create an API for the website so that clients can query the site with an existing list + seed user and have returned a list of items arranged into categories: accepted, rejected, or pending. This service could potentially be monetized, x sats per query, to support the website and further development of the DCoSL protocol.

## Bounty: to be determined

