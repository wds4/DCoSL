Refactor Curated Lists as a website with better UX
=====

## Background

Curated Lists, one of the apps in the Pretty Good Apps desktop nostr client, is a proof of concept implementation of the DCoSL procotol and arguably the first ever implementation of decentralized knowledge curation.

In its current form, Curated Lists is functional but needs better UX to attract users. This series of bounties is to refactor the existing functionality of Curated Lists as a website. (Possibly later to add additional functionality, such as an API.)

# [Phase 1: Curated Lists explorer](./phase1.md)

Create a website where users can explore existing lists and list items. Comparable to lists.lol.

## Bounty: 10,000,000 sats

<hr />

The following phases may be restructured following the succussful completion of phase 1, and their bounties are to be determined.

# Phase 2: User sign-in and data submission

Allow users to sign in (getalby or some similar method) to that they can:
- make new lists
- add list items
- endorse/reject items
- endorse/reject curators

## Bounty: to be determined

# Phase 3: add Control Panel for the grapevine

There are a number of adjustable constants that are used when calculating. For Phase 1, default values will be used for all constants. For this phase, a control panel will be added which allows the user to adjust constants and observe the change in real time on list curation.

## Bounty: to be determined

# Phase 4: visualization of the grapevine

Graphical representation of the web of trust with the ability to review calculations

## Bounty: to be determined

# Phase 5: API

Create an API for the website so that clients can query the site with an existing list + seed user and have returned a list of items arranged into categories: accepted, rejected, or pending. This service could potentially be monetized, x sats per query, to support the website and further development of the DCoSL protocol.

## Bounty: to be determined

