rulesets
=====

Sets of rules that must be enforced for a graph to meet the criteria of a concept graph

# Background 

important concepts (need glossary entries):
- enforceability
- locality
- parallellization of micro actions
  
A ruleset is composed of (typically one, but potentially more than one) macro rule plus an associated collection of micro rules (usually lots). 

There are "macro" rules, like class thread criteria, and "micro" rules which typically are derived from one (or more?) macro rules.
- the number of macro rules should be minimized
- the "Enforceablity" of any given macro rule should be maximized (minimize the amount of computational work to enforce it)

Enforceability basically refers to how easy or difficult it is to enforce the macro rule via micro rules. This may be measured in computing power. Looking for certain patterns in a graph, for example, can be very computationally expensive. May be difficult to quantify; will vary depending on lots of factors, such as number of nodes in a graph, etc. Nevertheless, enforceability is probably one of the best guides we have when designing new rulesets.

Macro rules are intended to be as compact (to state and understand) as possible, and as few as possible. Only one macro rule is needed to estbalish the concept graph, and it can be fit into a tweet (reference). The grapevine may require an additional macro rule, not sure yet. Macro rules are also chosen in a manner so that they should be <i>enforceable</i> using some set of micro rules which meet the criteria as below. The ease of enforceabiliity of any given macro rule is 

Micro rules are intended to be encoded into algorithms and enforced. Each micro rule consists of a pattern and an action. Patterns means some pattern found in a concept graph, e.g. every instance of two nodes connected by an edge of some specific relationship type. Actions are intended to be changes, such as take the elements of an array in nodeA and add them to some specific spot in node B. Micro rules are designed with the following optimizations:
- micro rules are intended to be run in parallel. It should NOT matter what order they are run. (There may be some exceptions to this rule, but exceptions should be kept to a minimum.)
- patterns should be computationally easy to find. Most patterns look are path searches with only one link in the path, e.g. find every instance in a concept graph of nodeA-isASubsetOf-nodeB. A set of patterns that contains no pattern searches of more than a single (or perhaps some small number N) hop in the graph is called a 'local' pattern set (perhaps: N-local, where 1-local is desired). A ruleset that can be enforced with a local set of patterns is called a 'local' ruleset.
- actions should be computationally easy to execute.

The parallelization of micro actions ensures that concept graph can be tended in the background, with resources used when available, but processing can be put on hold when resources are required for some other purpose. 

It is postulated that various categories of background processing may correspond to distinct stages of sleep. In particular: background pruning of the concept graph is stage 2 sleep and slow wave sleep (in support of this, there is evidence that nonREM sleep improves small world properties of brain functional connectivity; need to review this literature, been a while, can't remember if stage 2 or sws); background processing of the grapevine is REM sleep (because dreams are value-laden, as is the grapevine). 

Micro rules usually are of the form: whevever you see Pattern X, execute some set of Actions Y_i (the order of which may or may not matter; usually it should not matter).

## Macro rules

### class thread criterion

This is the first and most important rule for the concept graph, worthy of being called the Fundamental Ruleset of the Concept Graph. 

### Property Tree Ruleset

This ruleset accompanies the utilization of JSON Schema into DCoSL. By useing this ruleset, an entire JSON Schema is constructed out of a property tree. An implementation of this ruleset entails adoption of specific word types (property, jsonSchema, more?) and relationshipType(s) (formerly, in plex: addToConceptGraphProperties. need a more compact name for this).  

### grapevine macro rules

Do there need to be additional rules to make the grapevine? Not sure yet. If so, the macro rule(s) will be chosen according to 

### analogies

An analogy is a large, complex pattern in a concept graph, the verification of which is difficult. It involves taking two or more patches and pointing out similarity of structure between the patches. Typically, the patches differ in some respect that renders the similarity a surprising or unexpected one. (Need to work out a detailed example of this.) Verification of an analogy is often difficult because of its opposition to some element of a tribal tapestry. The inability to see or expressed opposition or rejection of some analagy may be considered proofof computation in service to the tribal narraative, aprticularly when the relevant patches are altered for the purpose of rendering the analogy untrue.

## Micro rules 

work in progress 

example: wherever you see setA-isASubsetOf-setB, 

## rule violations 

There are situations where deviation from a ruleset may serve some purpose, particularly in service to a `tribal tapestry`. In short, accumulation of errors in a neuronal tapestry, via embracing some set of beliefs, serves as evidence of loyalty to the tribe, particularly when some error is computationally expensive to maintain. This turns into a variation on the idea of proof of work. 
