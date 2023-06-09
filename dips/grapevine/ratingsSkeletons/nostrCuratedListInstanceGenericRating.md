rating template title: Nostr Curated List Instance: Generic Rating
=====

## Skeleton

All null fields are expected to be filled out, except that setting regularSliderRating to null is used to erase a rating (e.g. if submitted on accident)

JSON A:

```json
{
    "ratingData": {
        "raterData": {
            "raterType": "nostrProfile",
            "nostrProfileData": {
                "pubkey": null,
                "name": null,
                "display_name": null
            }
        },
        "rateeData": {
            "rateeType": "nostrCuratedListInstance",
            "nostrCuratedListInstanceData": {
                "eventID": null,
                "name": null,
                "slug": null
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
                "regularSliderRating": null,
                "contextData": {
                    "transitivity": false,
                    "contextDAG": {
                        "slug": "genericRating"
                    },
                    "nostrParentCuratedListData": {
                        "eventID": null,
                        "slug": {
                            "singular": null
                        },
                        "name": {
                            "singular": null
                        }
                    }
                }
            }
        }
    }
}
```

## Example 1: accept/reject an item to a specific list in Curated Lists (testnet-1)

JSON B:

Note that in the below, the `nostrParentCuratedListData` fields (eventID, slug, name) (widget in the example) point to a word that is a list (has listData as a top level property).

```json
{
    "ratingData": {
        "raterData": {
            "raterType": "nostrProfile",
            "nostrProfileData": {
                "pubkey": "61f976cf57851e0c1757d8bd962652a9e42d878ab1f7df31336fe430e2612e78",
                "name": "joker4",
                "display_name": "Joker: Jack Nicholson"
            }
        },
        "rateeData": {
            "rateeType": "nostrCuratedListInstance",
            "nostrCuratedListInstanceData": {
                "eventID": "e5757d59fa75ae0239912b9157bc388518f5c923b0a51a105e05ab9e75f4e559",
                "name": "first test widget entry",
                "slug": "firstTestWidgetEntry"
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
                        "eventID": "ae641d5606f3ec710b135678810d4256fd2e92022896ca58d194c361c46d81f9",
                        "slug": {
                            "singular": "widget"
                        },
                        "name": {
                            "singular": "widget"
                        }
                    }
                }
            }
        }
    }
}
```

## Example 2: accept/reject a topic to the list of nostr topics in Curated Channels (testnet-2)

JSON C:

Note: in the below, the `nostrParentCuratedListData` fields (eventID, slug, name) indicate a version of `nostrTopic` which is not a list but a wordType (so top level property has wordTypeData but not listData). Technically I should probably make a new rating template for this; either that or add a field under nostrParentCuratedListData to indicate whether to expect listData or wordTypeData.

```json
{
    "wordData": {
        "slug": "ratingOf_football(American)-12c9_thumbsup_by_wds4-102f",
        "wordTypes": [
            "rating"
        ]
    },
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
            "rateeType": "nostrCuratedListInstance",
            "nostrCuratedListInstanceData": {
                "eventID": "3b49b0769d4efc25be0e21f101160a9eecb9401f8b4abaa7650789baa75012c9",
                "name": "football (American)",
                "slug": "football(American)"
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
                        "eventID": "ec9af0fa71b2f6c1e3556816ad7c06e6623069c04a6e486fc9312b0273697779",
                        "slug": {
                            "singular": "nostrTopic"
                        },
                        "name": {
                            "singular": "nostr topic"
                        }
                    }
                }
            }
        }
    }
}
```

## Example 3: Curated Channels app, testet-2, accept/reject a relationship between two topics

JSON D:

```json
{
    "wordData": {
        "slug": "ratingOf_relationship-e26dd9_thumbsup_by_wds4-102f",
        "wordTypes": [
            "rating"
        ]
    },
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
            "rateeType": "relationship",
            "relationshipData": {
                "eventID": "f5e18bd6548dffead953b4b98f208bc1d625f3bd577e9a45a6dfb39fc2e26dd9",
                "slug": "relationship_iPhones-527174_isASubcategoryOf-d7c849_smartphone-e11742_c482fa"
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
                        "eventID": "6a7794b2b1d1cb33c05473fe2a52f4460eec63311e851e3c3fa8e787ca7d88fb",
                        "slug": {
                            "singular": "relationship"
                        },
                        "name": {
                            "singular": "relationship"
                        }
                    }
                }
            }
        }
    }
}
```

