# Vantablack: A Regex Hexadecimal Turorial

If you've ever worked with web design, you've likely encountered hexadecimal color codes. These codes, like #ffff (white) or #000000 (black), define colors for websites. But how do we ensure that a color code is valid? This is where regex, or regular expressions, come into play.

## Summary

The regex /^#?([a-f0-9]{6}|[a-f0-9]{3})$/ is designed to validate hexadicimal color codes. It ensures the code is either 3 or 6 characters long, optionally starts with a #, and only contains valid hecadicimal characters (0-9, a-f).

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Boundaries](#boundaries)

## Regex Components

### Anchors

^
Marks the start of the string. Ensures matching begins at the start of the input. 

$
Marks the end of the string. Ensures no extra characters exist after the hex code. 

### Quantifiers

{6} and {3}
Specify the exact number of characters to match. {6} matches excacty 6 characters, while {3} matches exactly 3 characters. 

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
