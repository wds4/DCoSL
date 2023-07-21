Phase 1: User Experience
=====

The site will download all available kind: 9901 and 39901 events and display them in an easy to navigate fashion.

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
- optional: raw json corresponding to the `word` and nostr event (relevant to Bonus #2)

### seed user selection

After making selections for list and seed user, the site will display:
- basic list information, including list name, list description, the author of the list, and when it was created
- all items that have been submitted to that list, with the ability to view each item name, item description, author of the item, and date of submission

In addition, the viewer should be able to review all attestations relevant to the selected list. Attestations are submitted as kind: 39901 events. (Pretty Good Apps will make it easy for you to see how these events are formatted.) There are two types of attestations:
- endorse (or reject) an item as "belonging" or not belonging on the list to which it is submitted
- endorse (or reject) a user as being a trusted (or not) curator of that particular list

The options for seed user will consist of all users who have received attestations as Curators of that particulat list. In addition, the visitor should have the ability to add any arbitrary npub as seed user.

The above should have an easy to navigate UX. Notably, the actual curation of list items (segregation into accepted, rejected, and pending) does not need to be implemented until Phase 2. However, the UX of Phase 1 should be designed with Phase 2 in mind.
