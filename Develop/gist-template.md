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

|

Acts as an Or operator. Matches either the 6-character sequence or the 3-character sequence. 

### Character Classes

{a-f0-9}

Matches any character from a to f (case-insensitive) or any digit from 0 to 9 These are the valid caharacters for a hexadicmal color code. 


### Grouping and Capturing

()

Groups parts of kthe regex togeter. in this case, ([a-f0-9]{6}|[a-f0-9]{3}) groups the two valid patterns (6 characters or 3 characters).

### Bracket Expressions

#?

The ? after the # makes the hash symbol optional. Matches both  #123456 and 123456.


### Boundaries

These ensure that the regex matches the entire input string without any extra characters before or after the valid hex code.

Examples

 #123456
 
123456

#FFF

FFF

## Invalid Matches:

 #123456 (only 5 characters)

12345 (only 5 characters)

#1234567 (7 characters)

#xyz (invalid characters)

### Back-references


## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
