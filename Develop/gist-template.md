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

Anchors are special charactors that define the position within a string where a pattern must start or end. 

^

Marks the start of the string. Ensures matching begins at the start of the input. 

$

Marks the end of the string. Ensures no extra characters exist after the hex code. 

### Quantifiers

Specify how many instances of a character, group, or character class must be present in the input for a match to be found.

{6} and {3}

Specify the exact number of characters to match. {6} matches excacty 6 characters, while {3} matches exactly 3 characters. 

### OR Operator

You can match one option or another witin your regex patter with the OR Operator. Place the pipe symbol between the different options you want to match within a character class or regex pattern.

|

Acts as an Or operator. Matches either the 6-character sequence or the 3-character sequence. 

### Character Classes

A set of characters enclosed within square brackets "[]" where any one of those characters can be matched within a string, and in the context of hexadecimal, a character class like "[a-fA-f0-9]" would match any single hexadecimal digit, including both lowercase and uppercase letters 9a-f,A-F) and numbers (0-9)

{a-f0-9}

Matches any character from a to f (case-insensitive) or any digit from 0 to 9 These are the valid caharacters for a hexadicmal color code. 


### Grouping and Capturing

The use of parenthesis to define a section of a pattern as a group, allowing you to exrract specific parts of a matched string, like a hexadecimal value, and access them separately; essentially, it lests you isolate and capture specifiec parts of a larger patters witinin a regex, particularly useful when dwealing with complex data like hexadecimal color codes where you might want to acess the individual red, green, and blue components.

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

My name is Gypze, I am an enthusiastic junior developer passionate about learning web development and sharing my knowledge with others. With a growing skill set in HTML, CSS, and JavaScript, I am dedicated to creating tutorials that make complex concepts accessible to beginners. Feel free to check out more of my work and projects on GitHub; https://github.com/gypze. 
