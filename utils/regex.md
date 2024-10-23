
# Regular expression

_Source:_
_`https://en.wikipedia.org/wiki/Regular_expression`_ 
_`https://www.w3schools.com/jsref/jsref_obj_regexp.asp`_


A regular expression is a pattern of characters.
The pattern is used for searching and replacing characters in strings.

## Syntax

/pattern/modifier(s)

*Example:*
- /w3schools/i

Where:
- w3schools: The pattern to search for.
- /w3schools/: A regular expression.
- /w3schools/i: A case-insensitive regular expression

### Modifiers

Modifiers define how to perform the seach:

| Modifier | Description |
| -------- |:-----------|
| /g | Perform a global match (find all) |
| /i | Perform case-insensitive matching |
| /m | Perform multiline matching |


### Brackets
Brackets are used to find a range of characters:

| Bracket | Description | 
| ------- | :---------- |
| [abc]	 | Find any character between the brackets |
| [^abc] | 	Find any character NOT between the brackets |
| [0-9]	 | Find any character between the brackets (any digit) |
| [^0-9] | 	Find any character NOT between the brackets (any non-digit) |
| (x\|y) | Find any of the alternatives specified |


### Metacharacters
Metacharacters are characters with a special meaning:

| Character | Description |
| --------- | :---------- |
| .  |  Find a single character, except newline or line terminator | 
| \w | 	Find a word character | 
| \W | 	Find a non-word character | 
| \d | 	Find a digit
| \D | 	Find a non-digit character | 
| \s | 	Find a whitespace character | 
| \S | 	Find a non-whitespace character | 
| \b | 	Find a match at the beginning/end of a word, beginning like this: \bHI, end like this: HI\b | 
| \B | 	Find a match, but not at the beginning/end of a word | 
| \0 | 	Find a NULL character | 
| \n | 	Find a new line character | 
| \f | 	Find a form feed character | 
| \r | 	Find a carriage return character | 
| \t | 	Find a tab character | 
| \v | 	Find a vertical tab character | 
| \x | xx	Find the character specified by an octal number xxx | 
| \x | dd	Find the character specified by a hexadecimal number dd | 
| \u | dddd	Find the Unicode character specified by a hexadecimal number dddd | 


### Quantifiers

| Quantifier | Description | 
| ---------- | :---------- |
|  n+ | Matches any string that contains at least one n |
| n* | Matches any string that contains zero or more occurrences of n |
| n? | Matches any string that contains zero or one occurrences of n |
| n{X} | Matches any string that contains a sequence of X n's |
| n{X,Y}| 	Matches any string that contains a sequence of X to Y n's |
| n{X,} | Matches any string that contains a sequence of at least X n's |
| n$ | Matches any string with n at the end of it |
| ^n | Matches any string with n at the beginning of it |
| ?=n | Matches any string that is followed by a specific string n |
| ?!n | Matches any string that is not followed by a specific string n |



## Test expression 
https://regexr.com/

2:13