Phase 1: Curated Lists explorer
=====
Create a website where users can explore existing lists and list items. Comparable to lists.lol.

## Bounty: 10,000,000 sats

Two options:
- you create your own repo / website. Bounty paid once site fully functional.
- For additional 2,000,000 sats bonus: Build on my repository (AGPL-3.0) and I will host website on dcosl.com. Bounty (including bonus) paid once PR is accepted. 

Phase 1 website would be comparable to listr.lol, which allows users to explore existing NIP-51 lists but does not allow users to create new lists (currently that's done using other clients?). The main different between Curated Lists vs listr or other NIP-51-formatted lists is that NIP-51 lists are not curated. 

Users will be given two basic actions:
- select an existing list
- select a "seed" user

Upon selecting a list, the website will display list data: description, who submitted the list, and when. In addition, there will be a list of all items that have been submitted to the list.

Upon selecting a list and a seed user, the website will sort submitted items into three categories: ACCEPTED, REJECTED, and PENDING. The user will discover that changing seed user results in items being sorted differently. This will showcase DIP-01, which is one of the foundational principles of DCoSL.

## tech details

Data will be acquired via DCoSL testnet-1, with lists and list items kind 9901 and curator and item endorsements kind 39901 events. Currently, these notes can only be created using the Pretty Good Apps desktop client.

Probably the most challenging aspect of this will be the calculations that go into curation. 

## bonus

allow users to explore structures of notes -- useful for developers (+ 1,000,000 sats)

<hr />

The following phases may be restructured following the succussful completion of phase 1, and their bounties are to be determined.