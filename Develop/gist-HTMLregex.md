# Code Crafting with Regex (Matching an HTML)
Regular expressions (regex) are powerful tools for pattern matching within strings. In this tutorial, we'll delve into a specific regex designed to match HTML tags. Understanding this regex will empower you to parse and manipulate HTML content effectively in your web development projects.

## Summary

In this tutorial, we'll dissect the regex `/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/`, breaking down each component to unveil its purpose and functionality. From anchors that assert the start and end of the string to quantifiers capturing attributes within HTML tags, we'll explore how each element contributes to the overall pattern. This regex not only ensures the correct opening and closing of tags but also accommodates self-closing tags. We'll demystify character classes, examine the usefulness of flags for case-insensitive matching, and explore the concept of back-references for tag consistency. By the end, you'll have a comprehensive understanding of this regex and be ready to wield its power in your own projects.

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
    - [Back-references](#back-references)
  - [Author](#author)

## Regex Components
/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/
### Anchors
These ensure the tag starts with '<'.
``^<``
The `^` asserts the start of the string, ensuring that the tag begins at the beginning of the line.  The `<`, ensuring the tag starts with `<` and this `$` asserts the end of the string which ensures that the entire string adheres to the specified pattern.
### Quantifiers
These match any attributes present in the HTML tag.
``([^<]+)``
`(` and `)` captures the group that contains the following pattern.
This `[^<]+` matches one or more characters that are not `<`.  This is used to match any attributes in the HTML tag.
The `*` quantifier allows for zero or more occurrences of the preceding pattern, which allows it to have multiple attributes.
### OR Operator
This hanldes the closing part of the tag.
``(?:>(.*)<\/\1>|\s+\/>)``
This `(?:)` is a non-captruing group that includes the alternatives for the closing part of the tag. 
- `>(.*)<\/\1>` will match the the closing tag with the content inside.
  - `>` matches the closing bracket, which is just `>`.  
  - `(.*)` will capture the content inside the HTML tag.  
  - `<\/\1>` will ensure that the closing tag matches the opening tag by using the back reference `\1`
- `\s+\/>` handles the case of self-closing tags.
  - `\s+` matches one or more whitespace characters.
  - `\/>` matches the self-closing part of the tag
### Character Classes
Specifies the ranges of characters to match
``[a-z]`` This will match any lowercase letter from `a` to `z`
### Flags
Enables case-insensitive matching.
``/i`` - putting this in the end of the regex will enable case-insensitive matching.
### Grouping and Capturing
- `([a-z]+)` - This is a capturing group that captures one or more lowercase letters.
- `([^<]+)*` - another example of a capturing group that captures one or more characters that are not `<`.
- `(?:>(.*)<\/\1>|\s+\/>)` this represents a non-capturing group that contains alternatives for the closing part of the tag.
  - `>(.*)<\/\1>` This will capture the content inside the HTML tag.
  - `\s+\/>` this will handle the case of self-closing tags.
### Bracket Expressions
`[a-z]` this character class will specify the range of characters, as mentioned in the character classes and in this case lowercase letters from `a` to `z`.
### Greedy and Lazy Match
The `*?` part represents a lazy match, making the `*` quantifier match as few characters as possible.
### Back-references
`\1` is a back-reference.  In this regex, it refers back to the first capturing group.  `([a-z]+)` will ensure that the closing tag matches the opening tag
## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

Michael Carmelo is a Full Stack Web Development professional with a couple of projects under his belt ready to work.  If you would like learn more or get in touch with the author you can visit his github account at the following:  https://github.com/Carmetlo
