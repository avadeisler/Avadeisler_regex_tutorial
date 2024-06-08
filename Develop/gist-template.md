# REGEX Tutorial

As a coding student, I have created a tutorial explaining regex (Regular Expressions) so that we can understand the search pattern the regex defines

## Summary

A Regex or regular expression is a sequence of characters that define a search pattern. Usually such patterns are used by string-searching algorithms for "find" or "find and replace" operations on strings. It also looks for input validations. It is a technique commonly developed in theoretical computer science.

We'll look a a string of code using regex, this code looks for a match HTML tag.

Example: /^<([a-z]+)([^<]+)_(?:>(._)<\/\1>|\s+\/>)$/

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

The anchor is what starts and ends the regular expression. In the matching email code,

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/,

the anchors are the ^ and the $. This code is saying that we are looking for something that starts with:

^([a-z0-9_\.-]+)

And it has to end with:

.([a-z\.]{2,6})$.

The anchor means that if we are to find a match it has follow those initial guidelines.
It must start and end with the given parameters within the code. If it does not, then it is not a match.

### Quantifiers

A quantifier is used to determine how many times a specific character or group of characters needs to be present in order to have a match. For example, if we used the following code in our regex, xyz+ then this will match any string xy followed by at least one z. So, if we look at our code for matching the email:

([a-z0-9_\.-]+)

this will match any string that contains a-z, 0-9, \_, ., or -. The quantifier + means that it has to contain at least one of this in order to have a match.

### Grouping Constructs

Code example:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

We can talk about grouping constructs.

([a-z0-9_\.-]+) is the first group that appears in our regex. This must be true before moving on to "match" the next part of the code. ([\da-z\.-]+) is the second group that appears in our regex. ([a-z\.]{2,6}) is the third group that appears in our regex.

When matching, we have to make sure we are following the guidelines of the group before moving on to the next group.

### Bracket Expressions

Code example:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

We can talk about grouping and capturing.

[a-z0-9_\.-]

The guidelines for matching the group. For this code snippet, it can contain letters a-z, numbers 0-9, an underscore, hyphen, or period.

The period is an escaped character, so it required the backslash in order to be able to be matched.

### Character Classes

\d is present in the given matching email code and what it will match a single letter character, a-z, after the @ sign in the email address. Basically ensuring that a letter is matched after the @ in the email and not a number or special character.

### The OR Operator

It is not present in the code for the given matching email code, but in order to talk about the OR Operator, we will look at the following code for matching a hex code.

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

This is a regex for matching a hex code that uses the OR Operator. What this will do is it will match where it starts with the # and that has to come first followed by one of the following:

[a-f0-9]{6} which will match a 6 character long string that contains a combination of a-f letters and 0-9 numbers.

| OR Operator

[a-f0-9]{3} it will match a 3 character long string that contains a combination of a-f letters and 0-9 numbers.

### Flags

A regex flag is not used in the matching email code that is being used for this tutorial. A regex typically comes in the form:

/regex/

Where the slashes denote where the regex starts and ends. A flag can be used after the slash to give more guidelines for our matching. The flags are:

- g stands for "global" which will allow for matching all the instances within a string that follow the matching guidelines set in the regular expression.

- m stands for "multiline" which will search line by line rather than searching through a string as a whole.

- i stands for "insensitive" which will make the regular expression case-insensitive, so capitals and lower-case letters will not affect the matching.

### Character Escapes

A character escape represents a character that may not be able to be conveniently represented in its literal form.

According to the Java API documentation for regular expressions, there are two ways in which we can escape characters that have special meaning. In other words, to force them to be treated as ordinary characters.

- Precede a metacharacter with a backslash ( \ )

- Enclose a metacharacter with \Q and \E

## Author

This tutorial was created by Ava Deisler.

Conatct Ava:

[GitHub](https://github.com/avadeisler)
[E-mail](avadeisler@gmail.com)
