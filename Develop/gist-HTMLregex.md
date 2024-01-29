# Code Crafting with Regex (Matching an HTML)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

## Table of Contents
- [Code Crafting with Regex (Matching an HTML)](#code-crafting-with-regex-matching-an-html)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [OR Operator](#or-operator)
    - [Character Classes](#character-classes)
    - [Flags](#flags)
    - [Grouping and Capturing](#grouping-and-capturing)
    - [Bracket Expressions](#bracket-expressions)
    - [Greedy and Lazy Match](#greedy-and-lazy-match)
    - [Boundaries](#boundaries)
    - [Back-references](#back-references)
    - [Look-ahead and Look-behind](#look-ahead-and-look-behind)
  - [Author](#author)

## Regex Components
*/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/*
### Anchors
*These ensure the tag starts with '<'.*
``
^<``

### Quantifiers
*These match any attributes present in the HTML tag.
``([^<]+)*
``

### OR Operator
*This hanldes the closing part of the tag.
``(?:>(.*)<\/\1>|\s+\/>)
``
### Character Classes
*Specifies the ranges of characters to match
``[a-z]``
### Flags
*Enables case-insensitive matching.
``/i``
### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
