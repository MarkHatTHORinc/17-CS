# Understanding Regular Expressions
#          (RegEx)

A **regex**, which is short for **regular expression**, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input. 

## Summary

For example, the following regular expression can be used to verify that user input is a valid email address:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Each component of this regex has a unique responsibility to make sure that a user enters an email address that begins with an unspecified number of characters preceding the `@` symbol, followed by a domain.

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

In regular expressions, we use anchors to check if the matching symbol is the
starting symbol or ending symbol of the input string. Anchors are of two types:
The first type is the caret `^` that checks if the matching character is the first
character of the input and the second type is the dollar sign `$` which checks if a matching
character is the last character of the input string.

### Quantifiers

In regular expressions, quantifiers (also called braces) are used to
specify the number of times that a character or a group of characters can be
repeated. For example, the regular expression `[0-9]{2,3}` means: Match at least
2 digits, but not more than 3, ranging from 0 to 9.

### Grouping Constructs

Grouping constructs delineate the subexpressions of a regular expression and capture the substrings of an input string. You can use grouping constructs to do the following:

* Match a subexpression that is repeated in the input string.

* Apply a quantifier to a subexpression that has multiple regular expression language elements. For more information about quantifiers, see Quantifiers.

* Include a subexpression in the string that is returned by the Regex.Replace and Match.Result methods.

* Retrieve individual subexpressions from the Match.Groups property and process them separately from the matched text as a whole.

### Bracket Expressions

The main purpose of bracket expressions is that they adapt to the user’s or application’s locale. A locale is a collection of rules and settings that describe language and cultural conventions, like sort order, date format, etc. The POSIX standard defines these locales.

### Character Classes

With a “character class”, also called “character set”, you can tell the regex engine to match only one out of several characters. Simply place the characters you want to match between square brackets

### The OR Operator

Grouping and alternation are core features of every modern regular expression library. You can provide as many terms as desired, as long as they are separated with the pipe character: |. This character separates terms contained within each (...) group.

### Flags

Regular expressions may have flags that affect the search.

There are only 6 of them in JavaScript:

* i With this flag the search is case-insensitive: no difference between A and a (see the example below).
* g With this flag the search looks for all matches, without it – only the first match is returned.
* m Multiline mode (covered in the chapter Multiline mode of anchors ^ $, flag "m").
* s Enables “dotall” mode, that allows a dot . to match newline character \n (covered in the chapter Character classes).
* u Enables full Unicode support. The flag enables correct processing of surrogate pairs. More about that in the chapter Unicode: flag "u" and class \p{...}.
* y “Sticky” mode: searching at the exact position in the text (covered in the chapter Sticky flag "y", searching at position)

### Character Escapes

The backslash in a regular expression precedes a literal character. You also escape certain letters that represent common character classes, such as \w for a word character or \s for a space. 

## Author

Mark Harrison has years of experience in back-end server development and has managed many development teams. He is currently earning his certification as a Full Stack Developer using the MERN stack.
[Github](https://github.com/MarkHatTHORinc)
