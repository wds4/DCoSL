Phase 1: Curated Lists explorer
=====

STATUS OF THIS DOCUMENT: under construction

See Phase 1 overview (link).

## Functionality for Phase 1

In the Pretty Good Apps desktop client, users can submit to the nostr network the following four types of events:
- a list
- an item for any list
- endorsement of an item: an attestation that the specified item either *does* or *does not* belong on the list
- endorsement of user as a curator of a given list: an attestation that the specified user is *trusted* or *not trusted* to be a curator of the specified list.

Event IDs are used to reference lists, list items, and attestations.

Unlike NIP-51, there is no concept of a list owner. You do not have to be the author/creator of a list to submit an item to that list.

Lists and list items are submitted using kind 9901 (regular events). Attestations are submitted using kind 39901 (parameterized replaceable events). See [DIP-1101](https://github.com/wds4/DCoSL/blob/main/dips/networking/nostr/1101.md): publication of a word over nostr, and [DIP-1104](https://github.com/wds4/DCoSL/blob/main/dips/networking/nostr/1104.md): publication of an attestation over nostr.

Each event packages a json object called a `word` in the event's `content` field. The notion of a `word` is foundational to the concept graph section of the DCoSL protocol and is explained in the draft version for [DIP-100](https://github.com/wds4/DCoSL/blob/main/dips/conceptGraph/100.md). 

Examples of words for each of the 4 event types are provided below.

### Lists

Example of the `word` for a list of nostr clients:

```json
{
    "nostrCuratedListData": {
        "name": {
            "singular": "nostr client",
            "plural": "nostr clients"
        },
        "title": {
            "singular": "Nostr Client",
            "plural": "Nostr Clients"
        },
        "slug": {
            "singular": "nostrClient",
            "plural": "nostrClients"
        },
        "description": "a list of all nostr clients",
        "propertyPath": "nostrClientData"
    },
}
```

Lists are referenced by their event IDs. This is to avoid problems where two users submit lists with the same name. (Imagine that Alice and Bob might each want to submit their own list called Users Who are Trolls and Scammers, but they may disagree on the proper description of what constitutes a troll or a scammer!)

### list items

Example of the `word` for an item submitted to the list of nostr clients:

```json
{
    "nostrClientData": {
        "name": "iris",
        "slug": "iris",
        "description": "Created by Martti Malmi. Not originally a nostr client, but switched over to nostr around Dec 2022."
    }
}
```

Note that in this example, the top-level property, `nostrClientData` must match `nostrCuratedListData.propertyPath` in the parent list (see example above). In addition, the nostr note for this list item contains an `e` tag which must match the event ID of the parent list to which it has been submitted. It is important to make sure that the parent event IDs match! This can become an issue if multiple lists are submitted with the same name.

### list item endorsements

For our purposes, all endorsements use a general-purpose json object with top-level property `ratingData`. 

Example of the `word` for one user's attestation that iris belongs on the list of nostr clients:

```json
{
    "ratingData": {
        "raterData": {
            "raterType": "nostrProfile",
            "nostrProfileData": {
                "pubkey": "a08175d65051c08b83600abf6f5c18efd455114b4863c65959c92b13ee52f87c",
                "name": "Darth McTesty",
                "display_name": "darthmctesty"
            }
        },
        "rateeData": {
            "rateeType": "nostrCuratedListInstance",
            "nostrCuratedListInstanceData": {
                "eventID": "d002689c55ccba5e09283dad16172dcce493c5c6e8c921bb13ed91f5075595f1",
                "name": "iris",
                "slug": "iris"
            }
        },
        "ratingTemplateData": {
            "ratingTemplateSlug": "nostrCuratedListInstanceGenericRating",
            "ratingTemplateTitle": "Nostr Curated List Instance: Generic Rating"
        },
        "ratingFieldsetData": {
            "ratingFieldsetSlugs": [
                "nostrCuratedListInstanceRatingFieldset",
                "confidenceFieldset"
            ],
            "confidenceFieldsetData": {
                "confidence": 80
            },
            "nostrCuratedListInstanceRatingFieldsetData": {
                "regularSliderRating": 100,
                "contextData": {
                    "transitivity": false,
                    "contextDAG": {
                        "slug": "genericRating"
                    },
                    "nostrParentCuratedListData": {
                        "eventID": "7e92c80fb7d3fa7bec453c8b3c6db306bdde50f7eee34e76a880fe0ab770d485",
                        "slug": {
                            "singular": "nostrClient"
                        },
                        "name": {
                            "singular": "nostr client"
                        }
                    }
                }
            }
        }
    }
}
```

Note that ratingTemplateSlug must be: `nostrCuratedListInstanceGenericRating`.

Note that the rater (Darth McTesty), the ratee (iris), the parent list (nostr clients) are identified by universally unique identifiers: the rater's pubkey, the ratee's event ID, and the parent list's event ID, respectively. The names and/or slugs are provided in this example, but MAY BE ABSENT (or old/obsolete, in the case of profile data) and cannot be assumed to be correct. Always use the unique identifier. If, for example, profile information for the rater cannot be located on the nostr network using the supplied pubkey, then use the above word's supplied name or display_name as a fallback (if not null).

Note also:
- The value of the field for confidence can be ignored. (For our purposes, it is set at the default value of 80%.)
- `regularSliderRating` will take only two values: 100, which indicates APPROVAL, and 0, which indicates REJECTION.

### endorsements of users as curators of a given list

Example of the `word` for one user's attestation that the user known as 'joker4' should NOT BE TRUSTED to curate the list of nostr clients.

```json
{
    "ratingData": {
        "raterData": {
            "raterType": "nostrProfile",
            "nostrProfileData": {
                "pubkey": "e5272de914bd301755c439b88e6959a43c9d2664831f093c51e9c799a16a102f",
                "name": "wds4",
                "display_name": "David Strayhorn"
            }
        },
        "rateeData": {
            "rateeType": "nostrProfile",
            "nostrProfileData": {
                "pubkey": "61f976cf57851e0c1757d8bd962652a9e42d878ab1f7df31336fe430e2612e78",
                "name": "joker4",
                "display_name": "Joker: Jack Nicholson"
            }
        },
        "ratingTemplateData": {
            "ratingTemplateSlug": "nostrCuratedListsCuratorEndorsement",
            "ratingTemplateTitle": "Nostr Curated Lists Curator Endorsement"
        },
        "ratingFieldsetData": {
            "ratingFieldsetSlugs": [
                "nostrCuratedListsCuratorEndorsementFieldset",
                "confidenceFieldset"
            ],
            "confidenceFieldsetData": {
                "confidence": 80
            },
            "nostrCuratedListsCuratorEndorsementFieldsetData": {
                "regularSliderRating": 0,
                "referenceRegularSliderRating": 100,
                "referenceData": {
                    "referenceEntityType": "nostrProfile",
                    "nostrProfileData": {
                        "pubkey": "e5272de914bd301755c439b88e6959a43c9d2664831f093c51e9c799a16a102f",
                        "name": "wds4",
                        "display_name": "David Strayhorn"
                    }
                },
                "contextData": {
                    "transitivity": true,
                    "contextDAG": {
                        "slug": "genericRating"
                    },
                    "nostrParentCuratedListData": {
                        "eventID": "7e92c80fb7d3fa7bec453c8b3c6db306bdde50f7eee34e76a880fe0ab770d485",
                        "slug": {
                            "singular": "nostrClient"
                        },
                        "name": {
                            "singular": "nostr client"
                        }
                    }
                }
            }
        }
    }
}
```

Note that the `ratingTemplateSlug` must be: `nostrCuratedListsCuratorEndorsement`.

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
