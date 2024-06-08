# Matching a URL - Regex Tutorial

In this tutorial, I will explain matching a URL regular expressions (Regex) using JavaScript. This is a field of Computer Science and can be helpful to coders at any stage in their coding journey. This tutorial can help users grasp a clearer understanding of regex components. The regex will be broken down in to different components to make understanding easier. 

## Summary

This tutorial will explain the regex below. The below regex is designed to match URLs. This includes domain names, paths, protocols, and formatting. The components that will be broken down include anchors, quantifiers, grouping constructs, bracket expressions, character classes, the OR operator, flags, and character escapes. 

Matching a URL Regex:

/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

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
What is are anchors?
Anchors are essentially symbols at the beginning and end of a regex. These are to show that the URL to be matched must adhere to the pattern between them. 
There are 2 main types of anchors, one for the start of the string, and the other for the end of the string. The starting anchor is ^ and the ending anchor is $ . 
For example, in the regex we are explaining, /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ , all of the content between /^ and $/ are the characters we are trying to match. Those characters being(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/? .
Anchors play a crutial role in the regex because it defines the pattern in the string that needs to be matched to the URL from beginning to end.

### Quantifiers
What are quantifiers? 
Quantifiers are symbols and characters that show how many times a part of hte regex should be repeated. You can write a quantifier if you want something to be repeated in the regex. 
There are many types of quantifiers that all symbolize different quantities. In the regex we are referring to, /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ , there are 4 quantifiers which are explained below. 
? : This quantifier means that the content before it is optional. In this case, the ? appears after (https?:\/\/)? which means the part of the URL (http:// or https://) is not necessary but can be included in the matching URL.
+ : This quantifier means that the domain name must have at least one character. This is found after ([\da-z\.-]+) and tells one or nore of the characters within the square brackets occurs.
{2,6} : This quantifier specifies how many characters the top level domain must have. This is seen in ([a-z\.]{2,6}) and means there must be between 2 and 6 characters in the top level domain.
* : This quantifier means that part of the path in the URL is optional. We see this after ([\/\w\.-]*) and it is saying that the part before occurs 0 or nore times meaning it might not happen, but it can happen.

### Grouping Constructs
What are grouping constructs?
Grouping constructs are enclodes in () and allow you to treat expressioons with multiple characters as a single unit. They have several purposes including keeping things organized and easy to handle.
In this case for matching a URL: /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ , there are 4 grouping constructs listed below. 
(https?:\/\/) : This is saying the URL can have but does not need to have the https or http
([\da-z\.-]+) : This is referring to the domain name and states it matches 1 or more letter, number, dor, or hyphen.
([a-z\.]{2,6}) : This states the URL matching regex has 2-6 copies of the sqeuence. 
([\/\w \.-]*) : This tells us that since there is a * after the grouping construct, it is being matched any number of times.

### Bracket Expressions
What is a bracket expression?
Bracket expressions are a large range of characters we want ot match in the regex. Using the bracket expressions can help simplify the information and shorten the regex since it stops is from having to type out characters individually.
For example, [a-m] means the same as [abcdefghijklm].
In our case, for matching a URL: /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ has 3 bracket expressions explained below. 
[\da-z\.-] : This means any numerical diget, lowercase letter from a-z, slash, dot, or hyphen, will match.
[a-z\.] : This means any lowercast letter from a-z, slash, or dot will match. 
[\/\w \.-] : This means any slash, any aplhanumeric character, or dot will match.

### Character Escapes
What are character escapes?
Character escapes stpically start with \ and are meant to be interpreted in a non-literal sense. These are meant to represent something. There are several charcter escapes, however there are only 2 used in matching a URL: /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
\d - This represents any numberical digit (0-9), and in seen in [\da-z\.-]
\w - This is seen [\/\w \.-] and means that it can be any aplhanumeric character to match in the URL.

## Author
I am currently a student in a coding bootcamp. Feel free to follow me on GitHub at https://github.com/cassiesprague