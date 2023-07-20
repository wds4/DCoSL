# Refactor the desktop app, Curated Lists, as a web app

## Background

Curated Lists, one of the apps in the [Pretty Good Apps](https://github.com/wds4/pretty-good) desktop nostr client, is an exploratory proof of concept implementation of the first steps of the protocol for [DCoSL: Decentralized Curation of Simple Lists](https://github.com/wds4/dcosl).

The ultimate goal of DCoSL is a roadmap to build tools for users to crowdsource data by delegating the curation of information to one's web of trust. To do this well is a complex problem, but one that I have put a lot of thought into over the years.

In its current form, Curated Lists is functional but needs better UX to attract users and gain visibility. A series of bounties is envisioned to refactor the existing functionality of Curated Lists as a website (and maybe eventually to add some additional functionality, such as an API).

Duplicate the existing functionality of the Curated Lists desktop app, currently part of the [Pretty Good Apps](https://github.com/wds4/pretty-good) nostr desktop client, as a web app. This will be broken down into multiple phases. Phase 1 will be a simple Lists explorer, to see what lists, list items, and attestations have been submitted to the network (via the PGA client), but without the full functionality of Curated Lists. The actual curation of the lists (determining which items are accepted or rejected by the reference user's web of trust) is more complex and will not be required to collect the Phase 1 bounty (but will probably be the core of Phase 2).

Needs to be great UX for the full bounty. Including with thought given to future dev of the site. We will pick someone to judge.

## Bounties: 
- [Phase 1](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1.md): 15,000,000 sats (+ up to 3,000,000 sats in bonuses; see below)
- [additional phases](https://github.com/wds4/DCoSL/tree/main/bounties/curatedLists): to be determined

## what I'm looking for

I'm looking for someone who is adept at web apps, react, and **most importantly: excellent at design and UX**.

Phase 1 should be relatively straightforward to implement for an experienced nostr developer with good UX skllls. To make it easy for you to bang this out quickly, I provide a [detailed overview](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1.md). If you're an experienced dev but new to nostr and looking to learn, this could be a good way to become familiar while stacking a few sats!

## More info

Please DM me npub1u5njm6g5h5cpw4wy8xugu62e5s7f6fnysv0sj0z3a8rengt2zqhsxrldq3 with questions, ideas, or words of encouragement! :-)

References:
- [DCoSL: Decentralized Curation of Simple Lists](https://github.com/wds4/DCoSL)
- [Pretty Good Apps](https://github.com/wds4/pretty-good)
- [details of Phase 1](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1.md)
- the [overview](https://github.com/wds4/DCoSL/tree/main/bounties) of DCoSL and Pretty Good Apps bounties (including a roadmap for future bounties beyond this one).
