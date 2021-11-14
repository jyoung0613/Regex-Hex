# Regex Hex

Tutorial for Regular expression matching a hex value.

## Summary

This tutorial will go over the regular expression for Matching a Hex Value:  `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

Regex is short for regular expression.  Regular expression uses symbols to create a search that will conform to the criteria written in your regex and will search your text to validate hex values.

Without knowing much about the characters and what they represent.  Its easy to see patterns already in the expression.

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

Patterns:
- `[a-f0-9]` happens twice and appears to do with the specific format of a hex value.
- `{6}{3}` two numbers appear relative to the points above, so they seem to work with the square bracketed information.
- `()` are very familiar in math, usually to do with an order of operations.
- `|` in programming the double-pipe or `||` represents an OR operator, so we can probably surmise that `|` is also used as an OR operator.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Author](#author)


## Regex Components

/ forward slash, `^` Caret, `#` Pound Symbol, `?` question mark, `()` parenthesis, `[]` square brackets,`a-f`, `0-9`, `{}` currly bracers, `|` pipe, and a `$` dollar sign

`/^#?` `( `[a-f0-9]` `{6}` `|` `[a-f0-9]` `{3}` )` `$/`

### Anchors
`^` is an anchor.  This does not carry a value that the regex useses to compair, but rather tells the expression that the string must begin with a pound sign `#`.  We have a `?` question mark however after the pound telling the expression that it does not have to start with a pound sign this giving us an or statement. Finally we have the `$` which helps close this expression once its done.  `/^#?` & `$/`

### Quantifiers
These allow for some flexibility in matching as they define the number of times a character, pattern or group appears in a regex match.  The quantifiers used in the matching hex value regex are the `[ ?` (Question mark also known as a special character, Matches Zero of one preceding character, and allows this regex search to start with a character other than `#`, `{6} {3}` (Currly Braces with a number will match exactly 6 characters for the first set and 3 characters for the second set)].

### OR Operator
The question mark `?` is not the only character that helps us with uncertainty by offering an alternate selection.  The `|` pipe is what we thought it was from above. It works as the || double pipes do in javascript giving us an or statement. So we have `([a-f0-9]{6}|[a-f0-9]{3})` which tells us the string can either have `6` characters with a pattern of `a-f0-9` or `3` characters with a pattern of `a-f0-9`.

### Character Classes
`[]`square brackets are considered a character class or set.  The information input inside these brackets will determine what your regex is looking for in its search.  You can use letters or numbers, you can even input a couple characters such as `ae` to find a misspelled work gr`ae`y in your text.

### Grouping and Capturing
The `()` parentheses characters are used for grouping in this regex as are the `[]` square brackets.  The `()` tell the express that everything inside has to be resloved before it can go outside the parentheses to continue evaluating the express.  In this case allowing the expression to close or exit.  The `[]` square brackets tell the expression the requirements for the values its checking. 

### Bracket Expressions
Refers to the `[]` square brackets in our regex that help define the criteria that the expression is trying to validate, and the `{}` curly brackets which tell the regex that it needs to have 6 characters where the second or statment allows for 3 characters.  `[a-f0-9]{6}|[a-f0-9]{3}` 

## Author
John Young is a Full Stack Developer that is excited to join the world through coding.  You can find all my work at https://github.com/jyoung0613