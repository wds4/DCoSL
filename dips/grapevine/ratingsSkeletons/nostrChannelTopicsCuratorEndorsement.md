nostrChannelTopicsCuratorEndorsement
=====

## Description

endorse a user as being a trusted (or not) curator of a given nostr topic. Curation here means: deciding which pubkeys to associate with which nostr topics.

rateeType: nostrProfile

contextData: nostrTopic; selector required in UX

transitive: yes

under nostrChannelTopicsCuratorEndorsementFieldsetData:
- referenceData should be the same as the rater in raterData (the rater is the reference)
- contextData.nostrTopicData indicates the nostr topic. If blank, it is understood to be the generic (top level) topic.

## JSON

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
