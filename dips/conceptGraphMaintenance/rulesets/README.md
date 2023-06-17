rulesets
=====

Sets of rules that must be enforced for a graph to meet the criteria of a concept graph

# Background 

A ruleset is composed of (typically one, but potentially more than one) macro rule plus an associated collection of micro rules (usually lots). 

There are "macro" rules, like class thread criteria, and "micro" rules which typically are derived from one (or more?) macro rules.
- the number of macro rules should be minimized
- the "Enforceablity" of any given macro ruls should be maximized.

Enforceability basically refers to how easy or difficult it is to enforce the macro rule via micro rules. This may be measured in computing power. Looking for certain patterns in a graph, for example, can be very computationally expensive. May be difficult to quantify; will vary depending on lots of factors, such as number of nodes in a graph, etc. Nevertheless, enforceability is probably one of the best guides we have when designing new rulesets.

Macro rules are intended to be as compact (to state and understand) as possible, and as few as possible. Only one macro rule is needed to estbalish the concept graph, and it can be fit into a tweet (reference). The grapevine may require an additional macro rule, not sure yet. Macro rules are also chosen in a manner so that they should be <i>enforceable</i> using some set of micro rules which meet the criteria as below. The ease of enforceabiliity of any given macro rule is 

Micro rules are intended to be encoded into algorithms and enforced. Each micro rule consists of a pattern and an action. Patterns means some pattern found in a concept graph, e.g. every instance of two nodes connected by an edge of some specific relationship type. Actions are intended to be changes, such as take the elements of an array in nodeA and add them to some specific spot in node B. Micro rules are designed with the following optimizations:
- micro rules are intended to be run in parallel. It should NOT matter what order they are run. (There may be some exceptions to this rule, but exceptions should be kept to a minimum.)

Micro rules usually are of the form: whevever you see Pattern X, execute some set of Actions Y_i (the order of which may or may not matter; usually it should not matter).

## Macro rules

### class thread 

This is the first and most important rule for the concept graph.

### grapevine macro rules

Do there need to be additional rules to make the grapevine? Not sure yet. If so, the macro rule(s) will be chosen according to 

## Micro rules 

work in progress 

example: wherever you see setA-isASubsetOf-setB, 

## rule violations 

There are situations where deviation from a ruleset may serve some purpose, particularly in service to a `tribal tapestry`. In short, accumulation of errors in a neuronal tapestry, via embracing some set of beliefs, serves as evidence of loyalty to the tribe, particularly when some error is computationally expensive to maintain. This turns into a variation on the idea of proof of work. 
