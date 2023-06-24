nostrChannelTopicContentCreatorEndorsement
=====

## description

Rate a pubkey as being one that provides content relevant to the specified topic. Note that the overall structure of this rating is very similar to that of nostrChannelTopicsCuratorEndorsement (with the exception of transitivity being false here, and as such, there also is no referenceData here), but has a different meaning.

## characteristics
- rateeType: nostr profile

## default scoring system 

"Thumbs UP" by default means that regularSliderRating = 100, confidence = 80.

"Thumbs DOWN" by default means that regularSliderRating = 0, confidence = 80.

The developer has the option to provide a more complex UI to give the user the option to adjust confidence and regularSliderRating scores (between 0 and 100 in each case).

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
            "ratingTemplateSlug": "nostrChannelTopicContentCreatorEndorsement",
            "ratingTemplateTitle": "Nostr Channel Topic Content Creator Endorsement"
        },
        "ratingFieldsetData": {
            "ratingFieldsetSlugs": [
                "nostrChannelTopicContentCreatorEndorsementFieldset",
                "confidenceFieldset"
            ],
            "confidenceFieldsetData": {
                "confidence": 80
            },
            "nostrChannelTopicContentCreatorEndorsementFieldset": {
                "regularSliderRating": null,
                "referenceRegularSliderRating": 100,
                "contextData": {
                    "transitivity": false,
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
