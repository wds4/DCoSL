slug: nostrCuratedListInstanceGenericRating

Title: Nostr Curated List Instance: Generic Rating


## applications: Curated Lists app

### use 1

- rate an item on a list; 100 = endorse, 0 = reject 

- context indicates the parent list

- item being rated is the ratee


## This template is also used in the Curated Channels app, although I probably ought to make two new templates for that purpose 

### use 1

- rate a topic, which is an item on the list of nostr topics (testnet-902, not testnet-901; technically not a list, but a wordType)

- ratee type is nostrCuratedListInstance -- ought to change this to nostrTopic

- context indicates the name of the list, which is nostrTopic

### use 2: rate a relationship

- ratee indicates which specific relationship

- ratee type is relationship; ought to be a subset of relationships, speficially the subset corresponding to nostr topic subcategory relationships 

- context indicates the parent list, which is relationship
