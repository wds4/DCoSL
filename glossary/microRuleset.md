micro ruleset
=====

A `micro ruleset` is a set of [micro rules](microRule.md). It can be transcribed as follows:

```json
[
  ["pattern_i1", "action_j1"],
  ["pattern_i2", "action_j2"]
]
```

Usually, a micro ruleset is just one pattern with all of the actions that it triggers. As an example: in the following micro ruleset, all elements use the same pattern, with only the action differing from one pairing to the next.


```json
[
  ["pattern_i", "action_j1"],
  ["pattern_i", "action_j2"]
]
```
