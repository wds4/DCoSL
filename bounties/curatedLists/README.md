Refactor Curated Lists as a website with better UX
=====

## Background

Curated Lists, one of the apps in the Pretty Good Apps desktop nostr client, is a proof of concept implementation of the DCoSL procotol and arguably the first ever implementation of decentralized knowledge curation.

In its current form, Curated Lists is functional but needs better UX to attract users. This series of bounties is to refactor the existing functionality of Curated Lists as a website. (Possibly later to add additional functionality, such as an API.)

# [Phase 1: Curated Lists explorer](./phase1.md)

Create a website where users can browse existing Curated Lists and observe the results of curation using different seed users. Compare to [listr.lol](https://listr.lol) (plus the list curation calculations, minus the log in).

## Bounty: 10,000,000 sats -- or make an offer!

# [Phase 2: User sign-in and data submission](./phase2.md)

Allow users to sign in (standard nostr tools such as getalby) to that they can:
- make new lists
- add items to existing lists
- endorse/reject items
- endorse/reject curators

## Bounty: to be determined

# [Phase 3: add Control Panel for the grapevine](./phase3.md)

There are a number of adjustable constants that are used when calculating. For Phase 1, default values will be used for all constants. For this phase, a control panel will be added which allows the user to adjust constants and observe the change in real time on list curation.

## Bounty: to be determined

# [Phase 4: visualization of the grapevine](./phase4.md)

Graphical representation of the web of trust with the ability to review calculations

## Bounty: to be determined

# [Phase 5: API](./phase5.md)

Create an API for the website so that clients can query the site with an existing list + seed user and have returned a list of items arranged into categories: accepted, rejected, or pending. This service could potentially be monetized, x sats per query, to support the website and further development of the DCoSL protocol.

## Bounty: to be determined

