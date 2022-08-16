#  Match an Email using Regular Expression

Gathering information from users can be a tricky thing sometimes. We often want to validate that the input is valid. This tutorial will guide you through using a regular expression, or "regex", to match emails to ensure that they are of valid format. 

## Summary

The expressions can look daunting, but in this tutorial  we'll break it down and anaylze each portion to better understand the regex. As our guide, we will use the expression: 
<br>
## /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/  
<br>
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

<br>

    * /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/  

<br>

A regex is a literal, so the pattern must be wrapped with slash characters (/). 

### Anchors
The next portion to pay attention to are the anchors. The characters ^ and $ are the anchors in our example.

- ^ -  The caret anchor matches the beginning of the string.
- $ - The dollar anchor matches the end of the string.

So in our Match an Email regex, the string must start and end with something that matches the pattern: 
> **`[a-z0-9_\.-]`**. 
### Quantifiers

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)