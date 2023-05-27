# Understanding Regular Expressions: Matching an Email

Regular expressions, or "regex", are patterns used to match character combinations in strings. In this tutorial, we will dissect the regex used to validate an email address. The regex in question is `^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$`. Let's break it down together and understand how it works.

## Summary

The regex `^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$` is used to match a valid email address. It ensures that the email is in the correct format with proper characters before and after '@', and with a valid domain name.

## Table of Contents

- [Anchors](#anchors)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Quantifiers](#quantifiers)

## Regex Components

In this section, we'll break down the various components of our regular expression. Understanding these elements will help you comprehend how the regex works as a whole. We will look at Anchors, Grouping Constructs, Bracket Expressions, and Quantifiers.

### Anchors

`^` and `$` are the start and end of line anchors respectively. They ensure that the matching is done from the start to the end of the string.

### Grouping Constructs

The parentheses `()` are used for grouping and capturing characters. In our regex, we have three groups: 
- `([a-z0-9_\.-]+)`: This matches the local part of the email before the '@' symbol.
- `([\da-z\.-]+)`: This matches the domain of the email after the '@' symbol.
- `([a-z\.]{2,6})`: This matches the domain extension of the email.

### Bracket Expressions

Bracket expressions `[]` define a character class—a set of characters to match. 
- `[a-z0-9_\.-]` will match any lowercase letter, digit, underscore, dot or hyphen.
- `[\da-z\.-]` will match any digit, lowercase letter, dot or hyphen.
- `[a-z\.]{2,6}` will match any lowercase letter or dot, but between 2 and 6 times due to the `{2,6}` quantifier.

### Quantifiers

The plus sign `+` is a quantifier meaning one or more. So `([a-z0-9_\.-]+)` and `([\da-z\.-]+)` mean one or more of the characters in the bracket expressions.

## Author

This tutorial was created by Weston Baker. You can find more about the author and his work on his [GitHub profile](https://github.com/WesBaker0).
