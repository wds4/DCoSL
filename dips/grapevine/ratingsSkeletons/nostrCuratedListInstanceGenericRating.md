nostrCuratedListInstanceGenericRating
=====



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
