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
- users can submit relationships: category A is a subcategory of category B

attestations:


### Grapevine calculations
