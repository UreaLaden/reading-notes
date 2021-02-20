# Regex Notes 
[Home](README.md)

Regular expressions commonly referred to as regex allow us to extract information from any text by searching for one or more matches of a specific pattern or sequence. For example:


## Anchors - ^and$
![anchors](/img/anchors.png)

## Quantifiers - * + ? and {}
![quantifier](/img/quantifiers.png)

## OR operator - | or []
![OR Operator](/img/OR_operator.png)

## Character classes -\d \s and
![Character Classes](/img/Character_classes.png)

In order for special characters to be taken literally, the characters `^.[$()|*+?{\` must be escaped with a backslash.

## Flags
A regex usually come within the form `/abc/`, where the search pattern is delimited by two slash characters `/`. At the end we can specify a flag with these values(we can also combine them with each other):

- **g** (global) does not return after the first match, restarting the subsequent searches from the end of the previous match.

- **m** (multi-line) when enabled `^` and `$` will match the start and end of a line, instead of the whole string.

- **i** (insensitive) makes the whole expression case-insensitive (for instance `/aBc/i` would match `AbC`)

## Grouping - ()

![Groups](/img/grouping.png)

If we choose to put a name to the groups (using `(?<foo>..)`) we will be able to retrieve the group values using the match result like a dictionary where the keys will be the name of each group. 

## Bracket expressions - []

[Bracket Expressions](/img/bracket_expressions)

## Greedy and Lazy Match

The quantifiers (* + {}) are greedy operators, so they expand the match as far as they can through the provided test.

For example, `<.+>` matches `<div>simple</div>` in `This is a <div>simple div</div> test`. In order to catch only the `div` tag we can use a `?` to make it lazy: 

[Lazy Match](/img/lazy.png)

## Boundaries - \b and \B

`\b` represents an anchor like caret matching positions where one side is a word characters and the other sie is not a word character (for instance it may be the beginning of the string or a space character).

`\babc\b` performs a *whole words only* search

`\B` matches all positions where `\b` doesn't match and could be if we want to find a search pattern fully surrounded by word characters.

`\Babc\B` matches only if the pattern is **fully surrounded** by **word** characters.

## Look-ahead and Look-Behind - (?=) and (?<=>)

`d(?=r)` matches a *d* only if it is followed by *r*, but *r* will not be part of the overall match
`(?~r)d` matches a *d* only if it is preceded by an *r*, but *r* will not be part of the overall match

You're also able to use the negation operator

`d(?!r)` matches a *d* only if it is not follow by *r*, but *r* will not be part of the overall match
`(?<!r)d` matchs a *d* only if it is not preceded by *r*, but *r* will not be part of the overall match. 


### Source 
[Jonny Fox - Regex tutorial - A quick cheatsheet by examples](https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285)
