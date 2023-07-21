Phase 1: User Experience
=====

Upon completion of Phase 1, the website will download all available kind: 9901 and 39901 events from the nostr network and display them in an easy to navigate fashion. 

Analysis of the attestations and the sorting of list items (accepted vs rejected) is not required for Phase 1. However, the website design should take into account, as appropriate, the upcoming features that will be anticipated in [subsequent phases](https://github.com/wds4/DCoSL/tree/main/bounties/curatedLists).

Sign-in with a nostr key will not be required for Phase 1 (probably not until Phase 3).

Visitors to the site will be presented with two options:
- select an existing list 
- select a reference ("seed") user

### list selection

All valid lists should be selectable. 

For initial rollout, with only a small number of lists to choose from, a simple drop-down menu would suffice. But we should anticipate the number of lists to increases; it will therefore likely be desirable to create a UI that makes lists searchable by list name, list decription, author, date of submission, list event ID, and/or number of proposed items. 

Once phase 2 is implemented, several other curation-related parameters could also be useful for search, e.g. number of accepted items, number of rejected items, number of curators, etc.

Once a list is selected, the viewer should be able to explore list details, including:
- list name
- list description
- list author, with author details (icon, name, etc)
- date of list submission
- all items that have been submitted to that list, with the ability to view data for each item including item name, item description, author of the item, and date of submission
- optional: raw json corresponding to all relevant `words` and nostr events (if implementing Bonus #2)

In addition, the viewer should be able to review all attestations relevant to the selected list. Attestations are submitted as kind: 39901 events. There are two types of attestations:
- endorse (or reject) an item as "belonging" or not belonging on the list to which it is submitted
- endorse (or reject) a user as being a trusted (or not) curator of that particular list

### seed user selection

The options for seed user will consist of all users who have received attestations as Curators of that particulat list. In addition, the visitor should have the ability to add any arbitrary npub as seed user.

The above should have an easy to navigate UX. Notably, the actual curation of list items (segregation into accepted, rejected, and pending) does not need to be implemented until Phase 2. However, the UX of Phase 1 should be designed with Phase 2 in mind.
