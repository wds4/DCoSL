Curated Graphs
=====

Building upon the tools established in Curated Lists to allow decentralized curation of graphs. 

Users will be able to submit their own graph, with the following properties:
- graph name
- graph description
- preexisting Curated List (specified using event ID or some other universal unique identifier)
- preexisting Relationship Type (an item on the Curated List of Relationships; specify using event ID or some other UUI)

Users will be able to submit items to the list, using the tools already established in Curated Lists. In addition, users will be able to submit new relationships, which take the form: (item A) - (relationship type) - (item B). (Technically, a relationship will be an item on the list of Relationships, which is a complex list; complex bc it has multiple properties. [one for item A, one for relationship type, one for item B].)

An example would be:
- graph name: Topics Tree
- graph description: This graph will be used to organize a tree of Nostr Topics so that your nostr feed can be organized into Channels.
- curated list: Nostr Topics
- relationship type: is a subcategory of (e.g.: Nost Topic: Smartphones - is a subcategory of - Nost Topic: Electronics)

Relevant DIPs are in progress.

# Phase 1: Curated Graph explorer

Users can explore existing Curated Graphs and view curation using different seed users but cannot sign in or add new data. Sample data will need to be created by the developers for this phase.

# Phase 2: 

- create new Curated Graph
- add items to the associated Curated List
- add relationships using the associated Relationship Type

# Phase 3: 
