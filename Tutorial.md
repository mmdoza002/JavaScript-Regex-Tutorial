# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

## Table of Contents

## Table of Contents:

1.	[Anchors](#Anchors)
2.	[Quantifiers](#Quantifiers)
3.  [OR Operator](#or-operator)
4.	[Character Classes](#Character-Classes)
5.	[Grouping and Capturing](#Grouping-and-Capturing)
6.	[Bracket Expressions](#Bracket-Expressions)
7.	[Greedy and Lazy Match](#Greedy-and-Lazy-Match)
8.	[Author](#Author)
9.	[User Story](#User-Story)
10.	[Acceptance Criteria](#Acceptance-Criteria)

## Regex Components

### Anchors

The Anchors are always at the beginning and end of the string. For the example above, `^` is the symbol for the beginning and `$` is for the end.

```text
^               Matches any string that starts with
$               Matches a string that ends with 
```

### Quantifiers

Quantifiers communicate to the regex engine that it MUST match the Quantity of the character or expression to its LEFT. 
There are two types of Quantifiers; Greedy and Lazy, each type has the same description.
- `* and *? `           Matches Zero or more times. 
- `+ and +? `           Matches One or more times.
- `? and ?? `           Matches Zero or One times.
- `{n} and {n}? `       Matches exactly n times.
- `{n,} and {n,}?  `    Matches at least n times.
- `{n,m} and {n,m}? `   Matches from n to m times.

Examples include:

```text
https?          Because of the `?` Matches 'https', 'http'. 
[\da-z\.-]+     Because of the `+` it matches a single digit, group of letters (a-z), dot (.) or hyphen (-) 1 or more times
[a-z\.]{2,6}    Because of the `{2,6}` it matches 2 to 6 copies of the sequence [a-z\.]
[\/\w \.-]*     Because of the `*` it matches '/', '.', '-', 'www', '//'
```

### Grouping Constructs

### Bracket Expressions

### Character Classes

Character Classes ensure that a given sequence of characters matches a Larger set of characters. 


```text
[a-z]          Matches lowercase alphabetic characters between a and z
\w             Matches a single word
\d             Matches a single character that is a digit 0-9
.              Matches any character
```

### The OR Operator

The purpose of an OR operator is to match the characters on the left or right of the operator, essentially serving as an or, as in and/or. Using the | as in m|M would match either m or an M from the string. If we had used ```https?:\/\/(www\.)?[\d-a|A``` it would search for a OR A.

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
