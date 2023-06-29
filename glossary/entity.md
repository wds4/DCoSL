Entity
=====

There are two definitions of entity in use. 

### Definition 1

An entity is any thing that controls a private cryptographic key and is capable of standard cryptographic functions, including signing, encryption, and decryption.

The most frequently encountered subset of entities is users. Generally speaking, a user is understood as an entity who is a person. However, given the widespread use of bots, a user may be defined as any entity who either is, or who pretends to be, a person. Other types of entities might include any AI. Some might advocate for the term user to be used in place of of the term entity.

### Definition 2

A second definition of entity is: any thing that can be the "ratee" of a rating. For any given rating JSON, the field: `ratingData.rateeType` would typically be something like user, movie, restaurant, etc and would refer to a particular type of entity. This informs the parser how to look for the ratee identifier, e.g. `ratingData.nostrUserData.pubkey` when `rateeType` = `nostrUser`.
