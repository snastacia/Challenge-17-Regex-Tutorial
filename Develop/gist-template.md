# Computer Science for JavaScript Challenge: Regex Tutorial

## Summary

Regular expressions (regex) are great tools for pattern matching and searching within text. In this tutorial, we will explore the process of matching an email address using regex. We will break down each part of the expression and describe what it does, helping you understand the inner workings of a typical email regex pattern.

The regex pattern we will be describing is designed to match a valid email address. Here is the code snippet of the regex:

const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;

This regex pattern can be used to validate email addresses and ensure they follow a specific format. Throughout this tutorial, we will explain the different components of this regex and their functionalities.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

Anchors are used to specify the position of the match within the text. In the email regex pattern, we use the ^ and $ anchors:

const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;

-The ^ anchor matches the start of a line.
-The $ anchor matches the end of a line.

By using these anchors, we ensure that the entire email address matches the pattern from start to end.

### Quantifiers

Quantifiers define the number of occurrences of a specific element in the regex pattern. In the email regex pattern, we use the + and {2,} quantifiers:

const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;

- The + quantifier matches one or more occurrences of the preceding element.
- The {2,} quantifier matches two or more occurrences of the preceding element.

In this case, we use the + quantifier to match one or more characters in the username part of the email address. The {2,} quantifier is used to ensure that the top-level domain (TLD) has at least two characters.

### OR Operator

The OR operator allows us to match either one pattern or another. In the email regex pattern, we use the | operator:

const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;

In this regex pattern, we use the | operator to match either a dot (.) or a hyphen (-) in the domain part of the email address.

### Character Classes

Character classes are used to specify a set of characters that can match at a specific position. In the email regex pattern, we use character classes like [a-zA-Z0-9._%+-] and [a-zA-Z]:

const emailRegex = /^[a

### Grouping and Capturing

Grouping in regular expressions allows you to treat multiple characters as a single unit. It enables you to apply quantifiers, capture specific parts of the pattern, or create logical sections within the regex.

In the context of matching an email address, grouping can be utilized to isolate the username, domain, and top-level domain (TLD) sections for further analysis or validation.

Let's consider the following regex pattern for email matching:

const emailRegex = /^([a-zA-Z0-9._%+-]+)@([a-zA-Z0-9.-]+)\.([a-zA-Z]{2,})$/;

In this pattern, we have three groups defined by parentheses ( ):

1. The first group ([a-zA-Z0-9._%+-]+) represents the username part of the email address. It allows alphanumeric characters, dots, underscores, percent signs, plus signs, and hyphens.
2. The second group ([a-zA-Z0-9.-]+) represents the domain part of the email address. It allows alphanumeric characters, dots, and hyphens.
3. The third group ([a-zA-Z]{2,}) represents the TLD part of the email address. It allows alphabetical characters with a minimum length of 2.
By grouping these sections, we can access and extract them individually for further processing.

## Author

This tutorial was created and authored by Nastacia Shershova, who is an aspiring Full Stack Web Developer currently enrolled in Columbia University's comprehensive Web Development Bootcamp.

Github: https://github.com/snastacia 
LinkedIn: https://www.linkedin.com/in/nastacia-shershova/ 
