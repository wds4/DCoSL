# Refactor the desktop app, Curated Lists, as a web app

## Bounties: 
- Phase 1 only: 10,000,000 sats
- additional phases: to be determined

## Overview

Duplicate the existing functionality of the Curated Lists desktop app as a web app. This will be broken down into multiple phases. Phase 1 will be a simple Lists explorer without full functionality. The actual curation of the lists (determining which items are accepted or rejected by your web of trust) will not be required to get the Phase 1 bounty.

## Background

Curated Lists, one of the apps in the [Pretty Good Apps](https://github.com/wds4/pretty-good) desktop nostr client, is an initial proof of concept implementation of the [DCoSL](https://github.com/wds4/dcosl) procotol, the ultimate goal of which is a general framework for the decentralized representation and curation of knowledge.

In its current form, Curated Lists is functional but needs better UX to attract users and gain visibility. A series of bounties is envisioned to refactor the existing functionality of Curated Lists as a website (and maybe eventually to add some additional functionality, such as an API).

Rather than improve the UX of the existing desktop client (UX being not my strong suit), I would like to focus on fleshing out the repo for the DCoSL protocol itself, which is woefully incomplete. For now, the best record of the protocol is its implementation the desktop client.

This 10 mil sat bounty refers to [Phase 1](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1.md), a basic Curated Lists explorer. Visitors to the site should be able to view existing Curated Lists and list items that have been broadcast as kind: 9901 and 39901 using the DCoSL protocol [DIP 1101](https://github.com/wds4/DCoSL/blob/main/dips/networking/nostr/1101.md), somewhat analogous to [listr.lol](listr.lol) for NIP-51 lists. Follow the [link](https://github.com/wds4/DCoSL/blob/main/bounties/curatedLists/phase1.md) for additional details.

## Functionality for Phase 1

Users will be presented with two options:
- select an existing list
- select a "seed" user
  
Existing lists will be those that have been posted as kind: 9901 events using the DCoSL protocol. Upon selecting a list, the website will display list data, including the list name, list description, who submitted the list, and when it was submitted. In addition, there will be a list of all items that have been submitted to the list.


See the [overview](https://github.com/wds4/DCoSL/tree/main/bounties) of DCoSL and Pretty Good Apps bounties (including a roadmap for future bounties beyond this one).
