
The most important property under `ratingData` is `ratingTemplateData`. The identity of the rating template dictates the structure of the other fields under `ratingData`; for example, whether the ratee type is nostr user or some other type of ratable entity.

```json
{
    "ratingData": {
        "ratingTemplateData": {
            "ratingTemplateSlug": null,
            "ratingTemplateTitle": null
        }
    }
}
```
