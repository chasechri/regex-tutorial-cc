# Regex Tutorial

In this tutorial I will be explaining the regex components in a expression so that you can understand how regex components function in matching a sequence of characters.

## Summary

In this tutorial I will be using an Email address expression to demonstrate how the different components of a regex function. The regular expression I will be using for matching an email is /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

This expression uses the anchor components ^ and $.

The ^ component asserts the position at the start of the string and the $

asserts the postion at the end. There will be an exact string match for everything between the ^ and $.

### Quantifiers

This expression uses the quantifiers {2,6}. This will match a string that ends with the previous token from 2 to 6 times.

### OR Operator

This expression uses the or operator []. This operator matches a string that contains a single character present within the [].

### Character Classes

In this expression the /d and . are used. The /d captures digits and the . matches any character. Grouped together they caputure all digits 0-9.

### Flags

In this expression the search pattern is delimited by the two slash marks at the beginning and end. You can set search criteria to mark the expression outside the flags in global (g), multi-line(m), or insensitive (i).

### Grouping and Capturing

In this expression there are 3 capturing groups created by the parentheses. The first is the username of the email, [a-z0-9_\.-]. The second is the captures the type of email being used, [\da-z\.-]. The third is the domain extension for the email, [a-z\.]{2,6}.

### Bracket Expressions

In this expression the brackets create borders within the parentheses. The first sets captures characters a-z, and numbers 0-9, and periods, underscores, or hyphens. The second set captures the same thing without underscores. The last set includes characters a-z and periods.

### Greedy and Lazy Match

The greedy qualifiers + and {} tell the expression to follow the match until the end of the expression.

### Boundaries

In this expression there are no boundaries. Boundaries can be created by adding a /b which would match postitions where one side is a word character and the other side is not.

### Back-references

Back references such as /1 would match the same text that was in the first capturing group and /2 would match the text of the second capturing group. There are no back references in this email expression.

### Look-ahead and Look-behind

There are no look-ahead or look-behind components in this email expression. A look ahead component would be c(?=h) would match a c only if it is followed by an h. A look behind component such as (?<=s)e would match an e only if an s comes before it.

## Author

This tutorial was created by Chase Christenson. GitHub link is: https://github.com/chasechri
