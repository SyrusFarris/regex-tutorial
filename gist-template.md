# Regex Tutorial Matching an Email

Regex is short for "regular expression" and is used to define a very specific search pattern using a sequence of characters. It is Regex's job genrally to validate users inputs.In this Regex tutorial we will focus on email address', but know that Regex is used to validate Hex Value's, URL's, and HTML Tag's as well. The goal of this tutorial is help developers develop a solid understanding on the email aspect of Regex.

## Summary

The regex code that will be analyzed is `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

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

Anchors are used to show where the expression starts and stops. In this case `^` to start, and `$` to identify where it stops.

### Quantifiers
In regular expressions there are 'Greedy' and 'Lazy' Quantifiers. This examples uses 'Greedy' quantifiers, `+` to signal another sequence needs to be matched as a 'Greedy' quantifier and also `{2,6}` as another 'Greedy" quantifier to signal the there should be a minimum of 2 charactors and a maximum of 6.

### OR Operator
The 'OR' operator is a alternation which can be denoted with the vertical line character `|`. An examply of this can be found in the following Hex value: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

### Character Classes
A character class is a notation that matches any symbol from a certain set. This is noted with `/d` and identifies the use of a digit from 0-9.

### Flags

Flags are can used to affect the search of Regular Expressions. For example `i`, this flag makes the search case-insensitive ("A" and "a").

### Grouping and Capturing

Grouping and capturing is identifed with parentheses. in our email example, these sections are grouped: `([a-z0-9_\.-]+)` , `([a-z\.]{2,6})`. this allows for the regex to get part of the match as a sepreate item in the result array and if we put a quantifier after the parentheses, it applies to the parentheses as a whole.

### Bracket Expressions

Brackets indicate a set of characters to match. Individual characters between the brackets will match. In or email example : `[a-z0-9_\.-]`, `[\da-z\.-]`, `[a-z\.]`, the characters in between the brackets will be matched.

### Greedy and Lazy Match

In regular expressions there are 'Greedy' and 'Lazy' Quantifiers. Greedy quantifiers let the match expand as far as it needs using `+` and `{}`. While Lazy quantifiers only allows for the minimum number of times, `+?` and `{}`.

### Boundaries

A boundry, or word boundry, can be though of as a test. there are none in our email example, but generally they are represented with `\b`.

### Back-references

In regex a group can be referenced in the pattern using `\N`, where 'N' is the group number. We have no exmaples of this in our email exmaple.

### Look-ahead and Look-behind

When we need to find only the matches for a pattern that are followed or preceded by another pattern we use this syntax to accomplish this. For example `X(?=Y)`, which means look for 'X' but only match if it is followed by 'Y'.

## Author

I'm Syrus Farris and I really hope this tutorial help give you more understanding on how regex works for mathcing Email's

github:https://github.com/SyrusFarris
