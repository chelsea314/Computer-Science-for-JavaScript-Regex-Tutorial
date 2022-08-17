#  Match an Email using Regular Expression

Gathering information from users can be a tricky thing sometimes. We often want to validate that the input is valid. This tutorial will guide you through using a regular expression, or "regex", to match emails to ensure that they are of valid format. 

## Summary

The expressions can look daunting, but in this tutorial  we'll break it down and anaylze each portion to better understand the regex. As our guide, we will use the expression: 

<br>

    /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/  
<br>

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
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

    /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/  

<br>

A regex is a literal, so the pattern must be wrapped with slash characters (`/`). We can now examine all components of a regex.

## Anchors

The next portion to pay attention to are the anchors. The characters ^ and $ are the anchors in our example.

- `^` -  The caret anchor matches the beginning of the string.
- `$` - The dollar anchor matches the end of the string.

So in our Match an Email regex, the string must start and end with something that matches the pattern: 

> `[a-z0-9_\.-]` 

Anything inside of sqaure brackets represents a range of characters we want to match. These patterns can be referred to as ***bracket expressions*** or ***positive character groups***. Essentially, they define the characters the are allowed to be included. 

If we break down the positive character group from our Match an Email regex, we can create 3 different groupings.

- `[a-z]` -- The string can contain any **lowercase** letter between a - z. 
- `[0-9]` -- the string can contain any number between 0 - 9.
- `[_\.-]` -- the string can contain an underscore, slash, period, or hyphen special characters.

When inputting an email, it's important to know that the user can input any lowercase character from a-z, any number from 0-9, and special characters of an underscore, slash, period, or hyphen. These characters can be in any order. The pattern does not have to include all of the requirements, but must include at least one of them. 

The following examples fulfill the requirements of this regexL

- "animal"
- "an1ma1s-rul3"
- "animal.lover"

## Quantifiers

<br>

    /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

<br>

The quauntifiers set the limits of the string, or an individual section of the string, that your regex matches. They include the minimum and maximum number of characters that your regex is looking for. 

In our 'Match an Email' example, we have the following quantifiers:

> `{2,6}`

> `+`

This means that we want the email to look for the preceding pattern a minimum of 2 times and a maximum of 6 times. This quantifier means that the final bracket expression `[a-z\.]` has to be between 2 and 6 characters long and can include lowercase character `a-z`, and the dot special character `.`. 

Typically this would look something like, `.com` or `.net` when used in a valid email. 

The + quantifier will connect the email's three parts. 

> `username + @email-provider + .com`

## Character Classes


A character class defines a set of characters. In our example we have one character class:

- `\d` -- Equivalent to the bracket expression [0-9]

We see this class in the second subexpression of our regex: 

> `([\da-z\.-]+)`

In this section of the email, numbers (`0-9`), characters (`a-z`) and special characters, (`.-`) are valid inputs.

The backslash (`\`) in a regex escapes a character. For example, this is common when looking for special characters that are the same as a particular component of a regex as we see in the previous section. 

## Flags

## Grouping and Capturing

The way to group a regex is by creating ***subexpressions***. 

A ***subexpression*** is created by using partentheses `()`. The 'Match an Email' regex contains 3 subexpressions:

> `([a-z0-9_\.-]+)`

> `([\da-z\.-]+)`

> `([a-z\.]{2,6})`


## Bracket Expressions

## Greedy and Lazy Match

## Boundaries

## Back-references

## Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)