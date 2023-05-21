Crowdsourcing a schema
======

[schema](https://schema.org/docs/schemas.html)
------------------------------

## Overview 

This example presents a strategy to crowdsource an [extension](https://schema.org/docs/extension.html) to a [schema](https://schema.org/docs/schemas.html). For the sake of argument, we will assume this is a (purpose of platform? What topics to go in the schema?) This same strategy could be used for an extension covering any subtopic: [an autos extension](https://schema.org/docs/auto.home.html), [health-lifesci](https://schema.org/docs/health-lifesci.home.html), a [bibliography extension](https://schema.org/docs/bib.home.html), a reputation system extension, etc.

Aside on `going meta`. Below you see a list of lists. What if we were to crowdsource that list? Or what if we were to crowdsource the listItemProperties for one or more of those lists? This type of thing is called going 'meta'. (See a slightly different way to go [meta](https://schema.org/docs/meta.home.html), where it is noted that the implementation of schemas can itself be managed.) If a schema is one type of `data model` then taking the idea of a schema and 'going meta' would involve inventing a new list called data model, and you can end up with an entirely new data model. In theory, there is no end to the number of levels one could 'meta up'. 

## Lists

For any given application, some of the lists below may be managed by developers (who set a default list that cannot be edited), with other lists being farmed out to the community. Looking at the several extensions above, the auto and health-lifesci extensions would require lists 1-4 to be crowdsourced, while the bib extension would require only lists 1, 2, and 4.

The developer determines the properties for list items for each list.

`List 1`: types

listItemProperties:

`List 2`: properties

listItemProperties: allowedValueTypes (array), usedOnTheseTypes (array)

`List 3`: enumerations

listItemProperties:

`List 4`: enumeration members

listItemProperties:

`List 5`: dataTypes

listItemProperties:

default list: DateTime, Boolean, Number, Date, Time, Text

`List 6`: relationship types

listItemProperties: slug, description

default list: isAChildOf, isAPropertyOf

`List 7`: relationships

listItemProperties:

examples:

type A isAChildOf type B

property A isAPropertyOf type A

`List 7`: schema extension

default: autos, bib, health-lifesci


