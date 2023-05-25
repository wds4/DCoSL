word type
=====

As per DIP-???, [words](word.md) are organized into categories called `word types`.

As per (DIP-100?), a word of wordType = foo:
- should have a top-level property: `fooData`
- The array, `wordData.wordTypes` should include the element: `foo`

As per (list DIPs), there are a handful of basic word types essential for construction of a [concept](concept.md):
| word type | top level property |
| ----- | ----- |
| word | wordData |
| jsonSchema | jsonSchemaData |
| wordType | wordTypeData |
| superset | supersetData |
| set | setData |

As per DIP (???), a word of word type = `wordType` is a required node in a [class thread](classThread.md).

DIP-??? outlines several methods for specification of a new word type.
