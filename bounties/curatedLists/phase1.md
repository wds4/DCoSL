Phase 1: Curated Lists explorer
=====

Create a website where users can browse existing Curated Lists and observe the results of list curation using different seed users.

## Bounty: 10,000,000 sats

Two options:
- you create your own repo, run your own website. Bounty paid once site fully functional.
- For additional 2,000,000 sats bonus: Build on my repository (AGPL-3.0) and I will host the website (perhaps on dcosl.com). Bounty (including bonus) paid once PR is accepted. 

If you like, we can pick someone we both know in the community to be the judge for when the bounty has been met.

## Functionality

Users will be presented with two options:
- select an existing list
- select a "seed" user

Existing lists will be those that have been posted as kind: 9901 events using the DCoSL protocol. Upon selecting a list, the website will display list data, including the list name, list description, who submitted the list, and when it was submitted. In addition, there will be a list of all items that have been submitted to the list.

Upon selecting a list and a seed user, the website will sort submitted items into three categories: ACCEPTED, REJECTED, and PENDING. The user will discover that changing seed user results in items being sorted differently. This will showcase DIP-01, which is one of the foundational principles of DCoSL.

## tech details

Data will be acquired via DCoSL testnet-1, with lists and list items kind 9901 and curator and item endorsements kind 39901 events. Currently, these notes can only be created using the Pretty Good Apps desktop client. Relays that support NIPs (?) are suggested (-- currently included in default relays in PGA).

Probably the most challenging aspect of this bounty will be the calculations that support list curation. Calculations consist primarily of calculating trust scores for curators and item scores for submitted items, each score being a weighted average. A display of how these calculations are performed can be found on the Pretty Good Apps desktop client. For reference, see also (link to files in PGA repo).

## assistance

I will be available to bouty hunters to clarify how Curated Lists currently works. Currently I am in the process of fleshing out these details into the DCoSL protocol. Your questions will help me to make the protocol more clear and more thorough.

## bonus

allow users to explore structures of notes -- useful for developers (+ 1,000,000 sats)

