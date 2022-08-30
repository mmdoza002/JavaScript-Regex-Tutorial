# JavaScript-Regex-Tutorial
Developers write code, but they also *write about code*. I took a moment to search the web for tutorials about any of the subjects I learned so far in this course. I found thousands of tutorials written by developers of all skill levels, and this is what I came up with

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

Grouping expressions allows us to keep things more organized and easier to exact the characters of a given group. This is used with parentheses "()".

```text
(https?:\/\/)     This group is basically saying it allows the URL code to being with "http://", "https://" or none of them.
([\da-z\.-]+)     This group which is the domain name. It matches 1 or more numbers, letters, dots or hyphens. Ending it with a "+" linking it to the following line.
([a-z\.]{2,6})    Withe the + connecting this group together, this matches 2-6 copies of the sequences "[a-z\.]"
([\/\w \.-]*)     This group is is being matched as many times as they want because of the "*" at the end. 

```

### Bracket Expressions

Bracket expressions are expressions between "[]" brackets. In the example above, we have the following Bracket Expressions.

```text
[\da-z\.-]
[a-z\.]
[\/\w \.-]
```

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

A flag changes the default searching behavior of a regular expression. It makes a regex search in a different way.

A flag is denoted using a single lowercase alphabetic character.

In JavaScript regex, we have a total of 6 flags, each serving a different purpose.

| Flag  | Name             | Modifocation                                                |
|--     |------------------|-------------------------------------------------------------|
|   i   |  Ignore Casing   |      Makes the expression search case-insensitively.        |
|   g   |  Global          |      Makes the expression search for all occurrences.       |
|   s   |  Dot All         |      Makes the wild character . match newlines as well.     |
|   m   |  Multiline       |      Makes the boundary characters ^ and $ match the beginning and ending of every single line instead of the beginning and ending of the whole string.                                                                                  |
|   y   |  Stick           |      Makes the expression start its searching from the index indicated in its lastIndex property.                                                                      |
|   u   |  Unicode         |      Makes the expression assume individual characters as code points, not code units, and thus match 32-bit characters as well.                                                |

### Character Escapes

## Author

Martin Mendoza [GitHub](https://github.com/mmdoza002)