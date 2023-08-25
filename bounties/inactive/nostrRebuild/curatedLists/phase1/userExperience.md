Phase 1: User Experience
=====

Upon completion of Phase 1, the website will download all available kind: 9901 and 39901 events from the nostr network (`wss://nostr.fmt.wiz.biz`, `wss://nostr.zebedee.cloud`, and `wss://nostr.oxtr.dev` ought to have all of them) and display them in an easy to navigate fashion. 

Analysis of the attestations and the sorting of list items (into the accepted, rejected, and pending/undecided bins) is not required for Phase 1. However, the website design should take into account, as appropriate, the upcoming features that will be anticipated in [subsequent phases](https://github.com/wds4/DCoSL/tree/main/bounties/curatedLists).

Sign-in with a nostr key will not be required for Phase 1 (probably not until Phase 3).

Visitors to the site will be presented with two options:
- select an existing list 
- select a reference ("seed") user

## list selection

All valid lists should be selectable. 

For initial rollout, with only a small number of lists to choose from, a simple drop-down menu would suffice. But we should anticipate the number of lists to increase; it will therefore likely be desirable to create a UI that allows the user to narrow the selection of lists by list name, list decription, author, date of submission, list event ID, and/or number of proposed items.

Once phase 2 is implemented, several other curation-related parameters could also be useful for search, e.g. number of accepted items, number of rejected items, etc.

Once a list is selected, the viewer should be able to explore list details, including:
- list name
- list description
- list author, with author details (icon, name, etc)
- date of list submission
- all items that have been submitted to that list, with the ability to view data for each item including item name, item description, author of the item, and date of submission
- optional (if implementing Bonus #2): raw json corresponding to the `words` and nostr events for each piece of data

In addition, the viewer should be able to review all attestations relevant to the selected list. Attestations are submitted as kind: 39901 events. There are two types of attestations:
- endorse (or reject) an item as "belonging" or not belonging on the list to which it is submitted
- endorse (or reject) a user as being a trusted (or not trusted) curator of that particular list

## seed user selection

The list of seed users will depend upon which list is selected.

The options for seed user will consist of all users who have either authored (rater), or are the subject of (ratee), endorsements (whether for or against) as Curators of that particulat list. Thus, the seed user list will be composed of all pubkeys listed as either rater or ratee of a kind 39901 event, with `ratingTemplateSlug`: `nostrCuratedListsCuratorEndorsement`, as per [this explainer](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1/pgaFunctionality.md). In addition, the visitor should have the ability to add any arbitrary npub as seed user.

Once the seed user is selected, the site should display basic user profile information. 

When deciding how to arrange the data on the page, keep in mind that the main thrust of phase 2 will be for visitors to the website to observe that changing seed user results in the list items being sorted differently into the accepted, rejected, or pending bins. So perhaps put the seed user selector above the list of items? ... These are design questions, not my forte! The way I've arranged things in the desktop app is perhaps too cluttered. 

An idea to consider to make the UX cleaner is to make the seed user panel invisible if a list has not yet been selected. This will help direct attention of the website visitor to the first task, which is list selection.

## Future phases

When designing the UX, bear in mind the features of upcoming phases:

Phase 2 (anticipated):
- list items will be segreated into 3 bins: ACCEPTED, REJECTED, and PENDING, as per screenshots from Pretty Good Apps desktop client [here](https://github.com/wds4/pretty-good/blob/main/appDescriptions/curatedLists/exampleListCuration.md)
- graphical representation of the web of trust, as per screenshots [here](https://github.com/wds4/pretty-good/blob/main/appDescriptions/curatedLists/exampleListCurationGrapevine.md) (I used visjs for the graphs)
- a penel that shows how weighted averages are calculated for any given list item or curator

Phase 3: Users can sign in and submit:
- new lists
- items for any list
- endorsements of list items
- endorsements of users as curators 

Phase 4: the grapevine Control Panel 
