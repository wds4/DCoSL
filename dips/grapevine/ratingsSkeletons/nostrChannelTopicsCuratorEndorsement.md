nostrChannelTopicsCuratorEndorsement
=====

## Description

endorse a user as being a trusted (or not) curator of a given nostr topic. Curation here means: deciding which pubkeys to associate with which nostr topics.

To avoid confusion: nostrChannelTopicsCuratorEndorsement is relevant for a user to curate the content to a specific topic, NOT to determine whether a specific topic is a valid topic (which is the purvue of nostrChannelTopicsTreeStructureCuratorEndorsement).

## characteristics

- rateeType: nostrProfile
- contextData: nostrTopic; selector required in UX
- transitive: yes
- under nostrChannelTopicsCuratorEndorsementFieldsetData:
- - referenceData should be the same as the rater in raterData (the rater is the reference)
- - contextData.nostrTopicData indicates the nostr topic. If blank, it is understood to be the generic (top level) topic.

## default scoring system 

"Thumbs UP" by default means that regularSliderRating = 100, confidence = 80.

"Thumbs DOWN" by default means that regularSliderRating = 0, confidence = 80.

The developer has the option to provide a more complex UI to give the user the option to adjust confidence and regularSliderRating scores (between 0 and 100 in each case).

## JSON

JSON A:

```json
{
    "wordData": {
        "slug": null,
        "wordTypes": ["rating"]
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
            "rateeType": "nostrProfile",
            "nostrProfileData": {
                "pubkey": null,
                "name": null,
                "display_name": null
            }
        },
        "ratingTemplateData": {
            "ratingTemplateSlug": "nostrChannelTopicsCuratorEndorsement",
            "ratingTemplateTitle": "Nostr Channel Topics Curator Endorsement"
        },
        "ratingFieldsetData": {
            "ratingFieldsetSlugs": [
                "nostrChannelTopicsCuratorEndorsementFieldset",
                "confidenceFieldset"
            ],
            "confidenceFieldsetData": {
                "confidence": 80
            },
            "nostrChannelTopicsCuratorEndorsementFieldsetData": {
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
                    "nostrTopicData": {
                      "eventID": null,
                      "slug": null,
                      "name": null
                    }
                }
            }
        }
    }
}
```
