Refactor the Curated Lists desktop app as a website
=====

## Background

Curated Lists, one of the apps in the [Pretty Good Apps](https://github.com/wds4/pretty-good) desktop nostr client, is a proof of concept implementation of the DCoSL procotol and arguably the first ever implementation of decentralized knowledge curation, as per the [core principles of DCoSL](../../dips/coreProtocol).

In its current form, Curated Lists is functional but needs better UX to attract users and gain visibility. The goal of this series of bounties is to refactor the existing functionality of Curated Lists as a website (and maybe eventually to add some additional functionality, such as an API). 

Currently Phase 1 is the only bounty that has been finalized. Bounties for subsequent phases will be finalized upon the successful completion of Phase 1.

# [Phase 1: a basic explorer for lists, list items, and attestations](./phase1/phase1.md)

Create a website where users can browse existing lists, list items, and relevant attestations. Phase 1 implementation will be relatively straightforward and will not require detailed understanding of the complex aspects of the DCoSL protocol. Just download kind 9901 and 39901 events and display them with a good UX! The actual curation itself (segregation of items into bins according to whether they have been accepted or rejected by the reference user's web of trust) will not be implemented until Phase 2. 

# [Phase 2: Curation](./phase2.md)

After selecting a list and a seed user, visitors to the site will observe the results of list curation. Submitted list items will be divided into 3 bins: ACCEPTED, REJECTED, and PENDING. It will be especially important for visitors to the site to understand that different reference users see different curation results, as per [this example from Pretty Good Apps](https://github.com/wds4/pretty-good/blob/main/appDescriptions/curatedLists/exampleListCuration.md) and according to the dictates of [DIP-01](https://github.com/wds4/DCoSL/blob/336027ab4935c80804a381e05fb5181ea5bfd22c/dips/coreProtocol/01.md), one of the core principles of DCoSL.

Implementation of this phase will require a deep dive into the grapevine section of the DCoSL protocol. Although the protocol repo is still a work in progress, the [Pretty Good Apps client](https://github.com/wds4/pretty-good/tree/main) provides a working example to see how exactly these calculations are made.

One of the challenges of this phase will be that the weighted average calculations are iterative and in principle repeat indefinitely. Therefore, they can be energy hungry. Probably the best way to address this problem is to stop iterations once stable results have been obtained, and to start them back up only if there is some change to the input data (such as a change in the selection of the reference user).

# [Phase 3: User sign-in and data submission](./phase3.md)

Allow users to sign in to the website (using standard nostr tools such as getalby) to that they can:
- make new lists (kind: 9901)
- add items to existing lists (kind: 9901)
- endorse/reject items (kind: 39901)
- endorse/reject list curators (kind: 39901)

## Bounty: to be determined

# [Phase 4: add the grapevine Control Panel](./phase4.md)

There are a number of parameters that are used when calculating weighted averages and sorting list items into bins. Parameters include the default Curator Trust scores for unvetted users. For prior phases, default values will be used for all parameters. For this phase 4, a control panel will be added which allows the user to adjust these parameters and observe the change in real time on list curation, the goal being to give users an intuitive feel for how these parameters work. This can be modeled after the control panel currently in use in Pretty Good Apps.

## Bounty: to be determined

# [Phase 5: visualization of the grapevine](./phase5.md)

Graphical representation of the web of trust with the ability to review the calculations of weighted averages for individual List Curators and List Items. Currently, the visjs javascript library is used by Pretty Good Apps for visualization. This or some other method may be used for this bounty.

## Bounty: to be determined

# [Phase 6: API](./phase6.md)

Create an API for the website so that clients can query the site with an existing list + seed user and have returned a list of items arranged into categories: accepted, rejected, or pending. This service could potentially be monetized, x sats per query, to support the website and further development of the DCoSL protocol.

## Bounty: to be determined

