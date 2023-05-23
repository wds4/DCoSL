
## This readme is under construction. 

Various examples (some hypothetical, some implemented) are discussed from the standpoint of the developer considering whether and how to use DCoSL to this particular problem.

Issues to be considered and decisions to be made for any given application:
<li>destination: the list of lists</li>
<li>the first list to be curated and the subsequent order of lists for rollout</li>
<li>loose consensus</li>
<li>DIP-1 and alternate methods of curation</li>

Also consider how to recognize what lists do not need to be curated, or at least should be low on the priority list.

# Who should implement this? How to get started?

Any developer working on any peer to peer platform, protocol, library, or tool. Think of some feature that your users may want to delagate to other users. Any feature can be broken down into a series of simple lists.

The first step, generally, would be to apply DCoSL to just one list. You, the developer, will create a default list, your own best guess as to what items should be on that list. Often, this may be a list that you, the developer, agoinze over, because you know that different users may have different ideas about what itms; belong on the list. So you give each user these options: use the default list; manage the list manually; or farm the list out to the WoT, using DIP-0 and perhaps other DIPs. If you are using DIP-0 by itself, you will write a bespoke method for list curation, typically using scraped data, e.g. a list of nostr relays scraped from the following list. Perhaps you agonize whether to expand one, two, three hops out? This decision can be farmed out to your user communities, using ideas from the DCoSL protocol.

The magic will become evident once additional, carefully chosen lists are added. Milestones can be created, defined by the things that your users can delegate. You may want to expand the simple list into a complex one, following DIPs below. Or you may wish to curate data models

Begin with the desired destination and then work backwards. That means: create a list of lists that together serve some function. Potentially, you will want to pick just one of the lists to offer for initial rollout to your users. Devise a method to curate that list. Provide an interface so that users have the following options: use the default list, curated by you, the team of developers; the user manages the list directly; or the users allows the web of trust to manage the list. Some intermediate states may be considered; for example, the WoT suggests updates to the list, which must then be approved manually, either individually or in aggregate, by the user. Once this is in place, then allow additional lists to be managed by DCoSL.

see examples 
