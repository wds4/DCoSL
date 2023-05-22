DIP-101
======

Complex Lists
------------------------------

## General principle

According to this DIP, users are given the ability to manage individually as well as to crowdsource complex lists.

A complex list is a simple list with one or more of the following associated 'auxiliary' lists (which may or may not hemselves be simple):

<li>a list of subsets</li>

<li>a list of subset relationships, of the form: subsetA isASubsetOf subsetB</li>

<li>a list of listItem properties</li>

each property is of propertyTypes: string, object, array, boolean, number, null

<li>a list of listItemPropertyRelationships, of the form: propertyA (relationshipType) propertyB</li>

with allowed relationshipTypes:
