nostrChannelTopicsTreeStructureCuratorEndorsement
=====

## Description

endorse a user as being a trusted (or not) curator of the nostr topic tree. This includes adding/removing topics from the list of topics and adding/removing topic relationships (topicA-isASubcategoryOf-topicB) to the list of relationships.

## characteristics 

rateeType: nostrProfile

contextData: none (other than transitivity); selector not required in UX

transitive: yes

referenceData: required (presumed for now to be the same as the rater)

## JSON

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
            "ratingTemplateSlug": "nostrChannelTopicsTreeStructureCuratorEndorsement",
            "ratingTemplateTitle": "Nostr Channel Topics Tree Structure Curator Endorsement"
        },
        "ratingFieldsetData": {
            "ratingFieldsetSlugs": [
                "nostrChannelTopicsTreeStructureCuratorEndorsementFieldset",
                "confidenceFieldset"
            ],
            "confidenceFieldsetData": {
                "confidence": 80
            },
            "nostrChannelTopicsTreeStructureCuratorEndorsementFieldset": {
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
                "transitivity": true
            }
        }
    }
}
```
