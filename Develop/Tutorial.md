# Regex Tutorial

Regex or regular expressions are patterns that are used to match strings. In javascript, they are also considered objects.

## Summary

The regex I will be going over here will be a pattern that searches for numbers. For example, if you wanted to validate a phone number with an area code, the format of a phone number would be 555-555-5555, each section being seperated by a hyphen, with 3 numbers in the first two, and four in the last. To do this, the expression would like this: `^\d{3}-\d{3}-\d{4}$`

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
The anchors of this expression are `^` and `$`. They give it a determined start and end.

### Quantifiers
Quantifiers (the {3} portion of this expression, or just {n}), instruct how many times something must be present for it to match. The {n} quantifier matches the preceding element exactly n times, where n is any integer.

### OR Operator
The `|` character can be used as an or. An example might be if someone included a country code in their phone number(such as +1 for the US) we would want to use the or operator to look for either one. So it would look like: `^\d{3}-\d{3}-\d{4} | \d{1}-\d{3}-\d{3}-/d{4}$`

### Character Classes
A character class allows your regex to match only one of several possible characters. Our regex uses \d to represent arabic numbers (0-9)

### Flags
A flag changes the default searching behavior of a regular expression. It makes a regex search in a different way. A flag is denoted using a single lowercase alphabetic character. In this example, we do not have a flag present, but more can be found here: https://www.codeguage.com/courses/regexp/flags

### Grouping and Capturing
We have no groupings in this example but some info on capturing can be found here: https://www.regular-expressions.info/refcapture.html

### Bracket Expressions
Curly braces are used to specify an exact amount of things to match. They are used after an expression: \na{2}\ will only match ‘na’ exactly twice.

### Greedy and Lazy Match
Greedy matches are called this due to trying to match as many elements as possible, as opposed to lazy which tries to match as few as possible. An example using our situation would be adding a ? to the expression. For example: `^\d{3}?-\d{3}?-\d{4}?$` would be adding lazy matches to each portion. Microsoft has a great article here, which while the code snippets are in C#, is quite detailed: https://learn.microsoft.com/en-us/dotnet/standard/base-types/quantifiers-in-regular-expressions#Greedy

### Boundaries
We do not use any boundaries in this, however a word boundary would be an operator that searches for a letter at the beginning or end of a string. For example, if you had the phrase "Hello World" and wanted to replace the letter H only if it starts or ends with it, you would use a boundary.

### Back-references
Backreferences can be used to match the same string more than once. There are none in this expression but an article can be found here: http://www.blackwasp.co.uk/RegexBackreferences.aspx
### Look-ahead and Look-behind
Look-ahead and Look-behind can be used to determine if a character can be found either ahead (to the right of), or behind (to the left of) and either succeeds or fails. While there isn't one in this expression, resources can be found here: https://www.regextutorial.org/positive-and-negative-lookahead-assertions.php

## Author

Nelson is a junior developer nearing completion of a full-stack developer bootcamp. You can [view my github profile](https://github.com/NelsonD93) for more of my work!
