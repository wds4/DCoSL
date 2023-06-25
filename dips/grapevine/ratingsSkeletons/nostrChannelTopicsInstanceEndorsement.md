nostrChannelTopicsInstanceEndorsement
=====

## description

Accept or reject a proposed nostr topic as being an instance on the list of nostr channel topics, parent event id: ec9af0fa71b2f6c1e3556816ad7c06e6623069c04a6e486fc9312b0273697779 (event might be updated)

## characteristics
- rateeType: an instance of the concept: nostrTopic
- contextData: parent concept is fixed: nostrTopic, event id: ec9af0fa71b2f6c1e3556816ad7c06e6623069c04a6e486fc9312b0273697779
- transitive: no

## default scoring system 

"Thumbs UP" by default means that regularSliderRating = 100, confidence = 80.

"Thumbs DOWN" by default means that regularSliderRating = 0, confidence = 80.

The developer has the option to provide a more complex UI to give the user the option to adjust confidence and regularSliderRating scores (between 0 and 100 in each case).

## JSON

JSON A: (new)

```json
{
    "wordData": {
        "slug": null,
        "wordTypes": [
            "rating"
        ]
    },
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
            "rateeType": "nostrChannelTopicInstance",
            "nostrChannelTopicInstanceData": {
                "eventID": null,
                "name": null,
                "slug": null
            }
        },
        "ratingTemplateData": {
            "ratingTemplateSlug": "nostrChannelTopicsInstanceEndorsement",
            "ratingTemplateTitle": "Nostr Channel Topic Instance Endorsement"
        },
        "ratingFieldsetData": {
            "ratingFieldsetSlugs": [
                "nostrChannelTopicsInstanceEndorsementFieldset",
                "confidenceFieldset"
            ],
            "confidenceFieldsetData": {
                "confidence": 80
            },
            "nostrChannelTopicsInstanceEndorsementFieldset": {
                "regularSliderRating": 100,
                "contextData": {
                    "transitivity": false,
                    "contextDAG": {
                        "slug": null
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
