# Matching Email Address with Regular Expression

Regular expressions (regex) are powerful tools for pattern matching in strings. In this tutorial, we will explore a regex pattern that can be used to validate and match email addresses.

## Summary

The regex pattern for matching an email address is `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. This pattern ensures that the email follows a standard format, including a valid username, domain, and top-level domain (TLD).

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

When using our email regex, `^` denotes the start of the string, ensuring that the match begins at the beginning of the email. Using the '$' symbol denotes the end of the string.

### Quantifiers

Quantifiers specify the number of occurrences of a character or group. Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. There
are quantifiers called greedy quantifiers ('*', '+', and '?' are examples). They are referred to as greedy because they cause a Regex pattern to take in as many accurences as 
possible. A lazy quantifier (using a '?' after a greedy quantifier) will cause a regex expression to gather the least occurences possible, thus the name "lazy."

### Grouping Constructs

Grouping constructs help organize and capture parts of the regex match. The parentheses in `([a-z0-9_\.-]+)`, `([\da-z\.-]+)`, and `([a-z\.]{2,6})` capture the username, domain, and TLD, respectively.

### Bracket Expressions

Bracket expressions define character sets. In email regex, these character sets define valid characters for the username, and domain. 
Here is an example of this: `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]`.

### Character Classes

Character classes represent a single character from a set. `\d` in `[\da-z\.-]` matches any digit in the domain.


### Flags

Flags modify the regex's behavior. The regex `/.../` does not include any flags, but modifiers like `i` for case-insensitivity could be useful.

### Character Escapes

Character escapes, such as `\.` in `\.([a-z\.]{2,6})`, are used to match literal characters like the dot (`.`).

## Author

[Emanuel Barroso]
GitHub Link: https://github.com/ebarroso24
