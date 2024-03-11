back to [Grapevine Curation Protocols main page](https://github.com/wds4/DCoSL/tree/main/grapevineCurationProtocols)

decentralized wikipedia
=====

## Synopsis

The Pretty Good Wiki (pgWiki) uses the Grapevine to enable you and your community to identify the most trustworthy domain-specific curators for your encyclopedia of content, facts, and information.

## Description

## Grapevine Curation Protocol

### data model

nodes: wikipedia articles

### user actions

#### content submission
- users can submit and edit a new wiki entry (replaceable event)

#### attestations
- user A can endorse (or block) User B as a curator for the wiki

### Grapevine calculations

# Rollout

## Phase 1

Problem: How do we weed out spam articles and edits?

Solution: Use follow lists and mute lists as raw data input into the simplest Grapevine algorithm: crowdscreened groups.
- Users are in one of three categories: whitelisted, blacklisted, or uncategorized
- If Alice follows (mutes) Bob, then Bob is on Alice's whitelist (blacklist)
- For any given user Bob, if N whitelisted users follow Bob and M whitelisted users mute Bob, then if N - M > 2, then Bob becomes whitelisted; or if M > N > 2, then Bob becomes blacklisted

## Phase 2

Problem: Just because Alice follows Bob doesn't mean she trusts him to curate wikis.

Solution: Introduce explicit attestations (as above). Use explicit attestation data in addition to follow and mute list data. Gradually phase out the usage of follow and mute lists as the explicit attestation dataset increases.

## Phase 3

Replace the simple Grapevine algorithm with the more sophisticated algorithm that is used in Curated Lists app of Pretty Good Apps.

## Phase 4

Introduce wikipedia categories.
