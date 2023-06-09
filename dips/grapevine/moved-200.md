DIP-200 (MOVED TO DIP-1104)
=====
publication of an attestation over nostr
-----

See also [DIP-100](../conceptGraph/100.md) for publication of a word over nostr.

Ratings, attestations, and endorsements are published as a Parameterized Replaceable Event as per [NIP-16](https://github.com/nostr-protocol/nips/blob/master/16.md) and [NIP-33](https://github.com/nostr-protocol/nips/blob/master/33.md) with kind in the range of 39000 - 39999. (Nothing below 39000 is used to avoid collision with NIPs, such as kind 30001 as per [NIP 51](https://github.com/nostr-protocol/nips/blob/master/51.md).

- kind 39901, with tag: `["g", "grapevine-testnet-901"]`
- kind 39902, with tag: `["g", "grapevine-testnet-902"]`
- mainnet is anticipated to use kind 39000, with tag: `["g", "grapevine"]`

### Tags

The multitude of tags, some with redundant information, are used to increase the number of search options.

| tag            | description                      |
| ---------------- | -------------------------------- |
| `g`              |  indicates grapevine              |
| `d`              |  uniqueID  |
| `r`              |  ratingTemplateUniqueID |
| `e`              |  the ratee, by event id |
| `l`              |  nostr event id of the parent list or concept |
| `m`              |  slug indicating the context of the rating |

where:

ratingTemplateUniqueID = ratingTemplate slug, ipfs hash, ipns name, nostr event id, or other unique identifier) -- context slug

uniqueID = rating author pubkey -- nostr event id of the parent list or concept -- ratingTemplateUniqueID

As examples, the item endorsement and curator endorsement from [DIP-01](../01.md) are packaged as follows:

The rating of the item is packaged into the following nostr event:

```json
{
    "kind": 39901,
    "tags": [
        ["g", "grapevine-testnet-901"],
        ["d", "61f976cf57851e0c1757d8bd962652a9e42d878ab1f7df31336fe430e2612e78-e5757d59fa75ae0239912b9157bc388518f5c923b0a51a105e05ab9e75f4e559-ae641d5606f3ec710b135678810d4256fd2e92022896ca58d194c361c46d81f9-genericContext"],
        ["r", "ae641d5606f3ec710b135678810d4256fd2e92022896ca58d194c361c46d81f9-genericContext"],
        ["e", "e5757d59fa75ae0239912b9157bc388518f5c923b0a51a105e05ab9e75f4e559"],
        ["l", "ae641d5606f3ec710b135678810d4256fd2e92022896ca58d194c361c46d81f9"],
        ["m", "genericContext"]
    ],
    "content": "{ ... }",
    ...other fields
}
```

The endorsement of the user as a curator is packaged as a nostr event:

```json
{
    "kind": 39901,
    "tags": [
        ["g", "grapevine-testnet-901"],
        ["d", "e5272de914bd301755c439b88e6959a43c9d2664831f093c51e9c799a16a102f-61f976cf57851e0c1757d8bd962652a9e42d878ab1f7df31336fe430e2612e78-ae641d5606f3ec710b135678810d4256fd2e92022896ca58d194c361c46d81f9-nostrCuratedListsCuratorEndorsement-genericContext"],
        ["r", "ae641d5606f3ec710b135678810d4256fd2e92022896ca58d194c361c46d81f9-nostrCuratedListsCuratorEndorsement-genericContext"],
        ["p", "61f976cf57851e0c1757d8bd962652a9e42d878ab1f7df31336fe430e2612e78"],
        ["l", "ae641d5606f3ec710b135678810d4256fd2e92022896ca58d194c361c46d81f9"],
        ["m", "genericContext"]
    ],
    "content": "{ ... }",
    ...other fields
}
```
    
# Search

To search for ratings or endorsements, use filters as in the following examples.

## Example

The following filter searches for ratings of items on the list of `nostr clients` published to testnet-1 with event id: `7e92c80fb7d3fa7bec453c8b3c6db306bdde50f7eee34e76a880fe0ab770d485`.

```
{
    "since": 0,
    "kinds": [
        39901
    ],
    "#g": [
        "grapevine-testnet-901"
    ],
    "#l": [
        "7e92c80fb7d3fa7bec453c8b3c6db306bdde50f7eee34e76a880fe0ab770d485"
    ],
    "#r": [
        "7e92c80fb7d3fa7bec453c8b3c6db306bdde50f7eee34e76a880fe0ab770d485-genericContext"
    ]
}
```

As of May 2023, ratings of list items always use the "genericContext". Additional contexts are anticipated in the future. 
