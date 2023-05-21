# Open Bazaar Rating Criteria for Listings

Background: The [OpenBazaar](https://github.com/OpenBazaar) rating system for listings, as enacted in OB 2.0, enables purchasers of a product to provide 5-star ratings of the product listing along 5 criteria: quality, delivery speed, customer service, description, overall. Phase 1 of this document outlines how DCoSL may be used to farm out the management of this list of criteria to the community. Phase 2 of this document outlines how DCoSL can be used to crowdsource a category tree for listings. Ratings criteria can then be crowdsourced uniquely for each listing category. For example: the rating criterion: `battery life` can be associated to the category of `smartphones`, with `acting`, `directing` and `screenwriting` associated with the category of `movies`. 

## Phase 1

Curation of the list of criteria for product ratings

DIPS: 00, 01

 The function of this phase is to allow users to farm out management of this list of criteria to their web of trust. More significantly, it lays the groundwork for subsequent phases (below).

### number of simple lists: 1

List 1: product listing criteria

Default list: quality, delivery speed, customer service, description, overall

Phase 1A: DIP-00

Users will manage their own list of criteria, which will be publicly accessible. Each criterion will have only one text field which is used as the unique identifier (the hashtag method). These lists will be scraped, so Alice can generate a locally curated list of criteria used by others in the network.

Phase 1B: DIP-02

Each criterion will have three fields: a cryptographic identifier, a name, and an optional description. Criteria will be published to the OB network, similar to the way listings are published. Any user can author criteria and can scrape them from the network, and can manage a local list of actively used and endorsed criteria. OB is built on top of an IPFS network, so either IPFS or IPNS can be used as the cryptographic identifier. IPNS might be useful to allow the author to update the description field. IPFS would be useful if it is desired for such changes to be impossible after publication.

Phase 1C: DIP-01

Users can endorse other users as trusted Curators of the list of criteria. These endorsements will be published to the OB network, similar to the way listings are published. Locally, a PageRank-like algorithm will be used to calculate an influence score for each user. These influence scores will be used as weights so that weighted average scores can be calculated for each criterion. Any criterion that rises above a threshold score will be placed into a user's local list of implemented criteria.

Observers will have the ability to monitor implemented criteria and assess the emergence of loose consensus.

## Phase 2

Management of a category tree for products

### number of simple lists: 2

List 1: a simple list of listing categories

Examples of categories:
```
{
  listingCatetoryData: {
    name: 'electronics',
    IPNS: 'abc123',
  }
}
```

```
{
  listingCatetoryData: {
    name: 'smartphones',
    IPNS: 'bcd234',
  }
}
```

List 2: a simple list of category relationships of the form: category A is a subcategory of category B. Categories will be identified using cryptographic identifiers (as opposed to the hashtag method).

Example category relationship:

```
{
  listingCatetoryRelationshipData: {
    categoryA: 'bcd234',
    relationship: 'isASubcategoryOf',
    categoryB: 'abc123',
    IPNS: 'xyz890',
  }
}
```

Vendors assign any given listing to one or more categories, using the context cryptographic identifier.

A unique list of rating criteria can now be associated to each category, and this list can be curated using the DCoSL method. For example: 

The category `smartphones` could have rating criteria: `battery life` and `durability`. 

Rating criteria are inherited down the context tree. For example, the criteria for the category of smatphones would be inherited by the subcategory of iPhones.


