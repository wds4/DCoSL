nostrCuratedListsCuratorEndorsement
=====

## skeleton backbone 

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
            "rateeType": "nostrProfile",
            "nostrProfileData": {
                "pubkey": null,
                "name": null,
                "display_name": null
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
                "regularSliderRating": null,
                "referenceRegularSliderRating": 100,
                "referenceData": {
                    "referenceEntityType": "nostrProfile",
                    "nostrProfileData": {
                        "pubkey": null,
                        "name": null,
                        "display_name": null
                    }
                },
                "contextData": {
                    "transitivity": true,
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

## Example: 

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
                "pubkey": "61f976cf57851e0c1757d8bd962652a9e42d878ab1f7df31336fe430e2612e78"
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
                "regularSliderRating": 100,
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
