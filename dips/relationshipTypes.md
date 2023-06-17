# relationship types

This is a summary of the basic [relationship types](../glossary/relationshipType.md).

## the concept graph

| relationship type | nodeFrom | nodeTo |
| ----- | ----- | ----- |
| isTheJsonSchemaFor | jsonSchema | wordType |
| isTheSupersetFor | superset | wordType |
| isASubsetOf | set | set |
| isASpecificInstanceOf | any | set |

## the grapevine

| relationship type | nodeFrom | nodeTo |
| ----- | ----- | -----|

## structural relationships

- conceptGraphs isASubsetOf graphs
- itemDirectories isASubsetOf graphs
- propertyDIrectories isASubsetOf graphs

concepts are not subsets of graphs, even though they serve a similar purpose as a collection of pointers to many words, because of the additional structure that you find inside conceptData.
