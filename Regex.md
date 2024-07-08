# Title 
Regex code for Email configuration

## Summary
Regular expressions (regex) are like a secret language for pattern matching within text. They allow you to define complex search patterns that can be incredibly powerful in data validation, text processing, and more examples! In this file, we explore a regex pattern designed to email addresses with international domain names include Unicode characters, making it more inclusive for various language scripts and symbols used in domain names worldwide. The regex is crafted to handle most email addresses with international domain names commonly seen in practice, each component will be broken down to its specific parts to further explain it!

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
^[\w.-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}(?:\.[a-zA-Z]{2,})?$
### Anchors
Anchors specify positions in the text where matches must occur, such as ^ for the start of the line and $ for the end of the line. This essentially closes in the code inside the regex line.Also '@ ' matches the literal  symbol.

### Quantifiers
Quantifiers specify how many instances of a character or group must be present for a match, like + for one or more occurrences . Here we use Non-capturing group with ? quantifier, making it optional.

### Grouping Constructs
Grouping constructs ( ) are used to create subexpressions within a larger regex, allowing you to apply quantifiers or capture matches.

### Bracket Expression
Bracket expressions [ ] define sets of characters to match against, such as [a-z] for any lowercase letter or [0-9] for any digit. We use these to define the parameters of the characters within each email address.

### Character Classes
Character classes \d, \w, and \s match digits, word characters, and whitespace respectively, providing shorthand for common character sets. We use \w for word characters to be included in the email address.

### The OR Operator
The OR operator | allows for matching one pattern or another, providing flexibility in specifying alternatives within a regex. We do not need to include this because in our bracket expressions, we already verify between capital and lowercase.

### Flags
Flags like i for case-insensitivity and g for global search modify how regex patterns are applied, altering the behavior of the regex engine. This is an email address only and not a password, meanng a flag is not needed.


### Character Escapes
Character escapes \ allow special characters to be used literally or give special meaning to characters that would otherwise be interpreted differently.We use this a few times in our code because it separates the different segments of the regex.

## Author

The Information was gathered by Parth Kapadia ,FrontEnd Developer Github Repo: https://github.com/ParthKapadia2207/Regex_email