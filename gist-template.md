# Regex Tutorial

Regular expressions are strings of text that can be used to search for other strings of text that meet certain criterias beyond just their literal values. They are special in that they can be used universally within any coding language. 

## Summary

The regex I will be breaking down is one that is used to find a string that matches an email address. /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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
The anchors in this regex are the characters ^ and $. The ^ anchor tells us that the string must begin with characters that match the criteria that immediately follows it. The same goes for the $ anchor except it works to make sure that the string ends with charachters that match the criteria that immediately precedes it.

### Quantifiers
We see two different Quantifiers being used in our regular expression.The first one is "+" and is used at the end of two of our grpuing constructs and means that the critreia must be matched one or more times. {2,6} tells us a minimum and maximum length of the string in which it is referencing. In this case, it is within the grouped expression ([a-z\.]{2,6}), so that specific expression must be a minimum of 2 characters and a maximum of 6 characters. 

### Grouping Constructs
Grouping constructs are used to match criteria to just a specific section of an expression. They are made by grouping sections within parenthesis. if you look at our regex for matching an email address, you'll see we have three grouping constructs each seperated by a literal value. 

### Bracket Expressions
Bracket expressions represent ranges of charachters that we want to be included in our search. If you look at our email matching regex you will see that each grouping construct has a bracket expression within it. the first bracket expression, [a-z0-9_\.-], requires that this subexpression must be made up of lowercase letters, any numbers, and the special characters "_", ".", and "-".

### Character Classes
Character classes are esentially a shorthand way of writing out longer expressions. The only character class we see in this regex is "/d" in the second bracket expression and it means that any arabic numeral digit. 

### The OR Operator
There are no OR operators in our email matching regular expression

### Flags
There are no flags in our email matching regular expression


### Character Escapes
character escapes are where we put "/" in front of a charachter that we want to include literally that would otherwise mean something else in a regular expression. We can see it being used in our regex multiple times to include the literal "." becuase without using the character escape it would be interpreted as a character class.

