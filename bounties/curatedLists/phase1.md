Phase 1: Curated Lists explorer
=====

STATUS OF THIS DOCUMENT: under construction

See Phase 1 overview (link).

## Pretty Good Apps functionality relevant to Phase 1

Follow [this link](pgaFunctionality.md).

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
