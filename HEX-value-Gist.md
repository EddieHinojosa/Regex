# Regex Tutorial for HEX values

Regex (Regular expressions) can help a tool used to match what youbare searching via text.
below will hvae a breakdown of how Hexadecimal values can be matched to finds the color you are looking for, including minimizing errors regarding cap sensitive input.

## Summary

<p>The purpose of hexadecimal (HEX) values is to pull a precise color located on the color wheel/block.</p>

<p>Below i'll explain a FULL breakdown of each section inside the given code: <br> 

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/ ` </p> as well as how to include input and what can be added to leverage less errors due to case sensitivity.</p>


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


## Regex Components

### Anchors

<p>Anchors are used to match positions within a string rather than actual characters. In the given regex:

* `^` asserts the position at the start of a line.
* `$` asserts the position at the end of a line.
</p>

### Quantifiers

<p>Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found.

* `{6}` specifies exactly 6 occurrences.
* `{3}` specifies exactly 3 occurrences.

</p>

### OR Operator

<p>The OR operator | allows you to specify multiple alternatives. In the regex:

`([a-f0-9]{6}  |  [a-f0-9]{3})` matches either 6 hexadecimal characters or 3 hexadecimal characters.</p>

### Character Classes

<p>Character classes match any one of a set of characters. They are defined using square brackets [].

`[a-f0-9]` <br>

matches any hexadecimal digit `(0-9, a-f)`. <br>


`[a-fA-F0-9]`<br>
matches any hexadecimal digit `(0-9, a-f, A-F)` when case insensitivity is included.</p>

### Flags

<p>Flags modify the behavior of the regex. The case-insensitive flag i makes the regex match letters regardless of case.

Adding `i` at theend: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/i` <br>

if the `i` is not included, it wont recognize the input due to it having to be EXACTLY the same<p>


### Grouping and Capturing

<p>Parentheses () are used for grouping and capturing. <br>

`([a-f0-9]{6}|[a-f0-9]{3})` groups the alternatives for either 6 or 3 hexadecimal digits.</p>


### Bracket Expressions

<p>Bracket expressions are used to specify a set of characters to match.

`[a-f0-9]` specifies any character in the range a-f or 0-9. </p>

### Greedy and Lazy Match

<p>Greedy matching tries to match as much of the input text as possible. Lazy matching tries to match as little of the input text as possible.

In the provided regex, all quantifiers are greedy by default `({6}, {3})`. </p>


### Boundaries

<p>Boundaries are used to match positions in a string. In the regex, the ^ and $ anchors mark the start and end boundaries of the string. </p>


## Author

created by EddieHinojosa @ [https://github.com/EddieHinojosa](https://github.com/EddieHinojosa)
