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

In regex, "anchors" are special characters that don't match any specific character but instead specify the position within a string where a pattern must start or end, ensuring the match occurs only at the beginning or end of a string, even when dealing with hexadecimal values; the most common anchors are "^" (beginning of string) and "$" (end of string).

^

Marks the start of the string. Ensures matching begins at the start of the input. 

$

Marks the end of the string. Ensures no extra characters exist after the hex code. 

### Quantifiers

In regex, a "quantifier" is a special character that specifies how many times a preceding pattern (like a hexadecimal character) should be repeated in a match, essentially defining the minimum and maximum occurrences of a pattern within a string; for example, in the regex [a-f0-9]{6}, the {6} is a quantifier, meaning it will match exactly six hexadecimal characters in a row

{6} and {3}

Specify the exact number of characters to match. {6} matches excacty 6 characters, while {3} matches exactly 3 characters. 

### OR Operator

In regex, including when dealing with hexadecimal values, the "Or Operator" is represented by the pipe symbol (|) which allows you to match a string that can fit either one of multiple patterns specified on either side of the pipe, essentially meaning "match this pattern OR match that pattern" within your regex expression

|

Acts as an Or operator. Matches either the 6-character sequence or the 3-character sequence. 

### Character Classes

In regex, a "Character Class" refers to a set of characters enclosed within square brackets "[]" that allows you to match any single character from that set, and in the context of hexadecimal, a character class would specifically match any single hexadecimal digit (0-9, A-F, or a-f) by using a range like "[0-9a-fA-F]" within the brackets, essentially allowing your regex to match any valid hexadecimal character.

{a-f0-9}

Matches any character from a to f (case-insensitive) or any digit from 0 to 9 These are the valid caharacters for a hexadicmal color code. 


### Grouping and Capturing

The use of parenthesis to define a section of a pattern as a group, allowing you to exrract specific parts of a matched string, like a hexadecimal value, and access them separately; essentially, it lests you isolate and capture specifiec parts of a larger patters witinin a regex, particularly useful when dwealing with complex data like hexadecimal color codes where you might want to acess the individual red, green, and blue components.

()

Groups parts of the regex togeter. in this case, ([a-f0-9]{6}|[a-f0-9]{3}) groups the two valid patterns (6 characters or 3 characters).

### Bracket Expressions

Using square brackets ("") to define a set of characters that includes all valid hexadecimal digits.

#?

The ? after the # makes the hash symbol optional. Matches both  #123456 and 123456.


### Boundaries

In regex, "boundaries" generally refer to the starting and ending points of a string, often marked by the "^" (caret) character for the beginning and "$" (dollar sign) for the end, and are not specific to hexadecimal values; they essentially define where a pattern must start and end within a string, ensuring the match occurs only at those precise positions

These ensure that the regex matches the entire input string without any extra characters before or after the valid hex code.

Examples

 #123456
 
123456

#FFF

FFF

## Invalid Matches:

In regex for hexadecimal values, "invalid matches" refer to any string that does not adhere to the proper format of a hexadecimal number, meaning it contains characters outside the range of 0-9 and A-F (or a-f), or has an incorrect structure like missing leading zeros or exceeding the allowed number of digits for the specific contex

 #123456 (only 5 characters)

12345 (only 5 characters)

#1234567 (7 characters)

#xyz (invalid characters)

### Back-references


## Author

My name is Gypze, I am an enthusiastic junior developer passionate about learning web development and sharing my knowledge with others. With a growing skill set in HTML, CSS, and JavaScript, I am dedicated to creating tutorials that make complex concepts accessible to beginners. Feel free to check out more of my work and projects on GitHub; https://github.com/gypze. 

-I did use Search Labs|AI Overvieww to help with the information given in this project.
