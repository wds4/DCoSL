back to [Grapevine Curation Protocols main page](https://github.com/wds4/DCoSL/tree/main/grapevineCurationProtocols)

Nostr Apps Directory
=====

## Synopsis

The Nostr Apps Directory enables you and your community to curate a list of Nostr Apps and to organize them into categories.

## Description


## Grapevine Curation Protocol

### data model

Extension of the [DCoSL](DCoSL.md) protocol library with the added restrictions:
- only one type of node is being curated: 

Extension of the [DCoG](DCoG.md) protocol library with the following restrictions:
- only two types of nodes are allowed: Nostr Apps and Nostr App Categories
- allowed relationship types: cat A isASubcategoryOf cat B
- nostr App X isASpecificInstanceOf category A

### user actions

create new instances
- users can submit Nostr Apps
- users can submit categories of Nostr Apps
- users can submit relationships: category A is a subcategory of category B (may be redundant given the ability to attest?)

attestations:
- that Nostr App X does / does not belong on the list of Nostr Apps
- that Nostr App Category A does / does not belong on the list of Nostr App Categories
- User A endorses User B as a trusted / not trusted curator of the Nostr Apps Directory
- that Category A is / is not a subcategory of Category B

optional attestations:
- that Nostr App X and Nostr App Y are the same (redundant)

### Grapevine calculations
