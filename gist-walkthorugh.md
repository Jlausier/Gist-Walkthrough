# Regex Matching a url

This is a tutorial to break down a regex. I have chosen to break down the regex for matching a url. This walkthorugh will break down everything contain in the regex and there purpose. 

## Summary

I will break down all the components within th e folowing REGex.  Matching a URL: `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/` . In summary, the provided regex pattern is used to match URLs, allowing for both "http" and "https" protocols, capturing domain names and TLDs, and optionally capturing path components. It employs a variety of regex components to achieve this comprehensive matching.

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

Anchors in regex are used to specify the position of the match in the input string. The pattern starts with ^ which signifies the start of the string, and it ends with $ which signifies the end of the string. This ensures that the entire string is matched from start to finish.

### Quantifiers

Quantifiers control how many times a specific element in the pattern can appear. In this regex, the quantifiers used are:

?: Matches the preceding element zero or one time. It's used after (https?:\/\/) to make the "s" in "https" optional.
*: Matches the preceding element zero or more times. It's used after ([\/\w \.-]*) to match any additional path components.

### Grouping Constructs

Grouping constructs are used to treat a group of characters as a single unit. In this regex:

(https?:\/\/)?: This is a non-capturing group that contains the protocol part of the URL, either "http://" or "https://://". The ? makes this group optional.
([\da-z\.-]+): This is a capturing group that matches the domain name part of the URL, which consists of one or more lowercase letters, digits, dots, and hyphens.
([a-z\.]{2,6}): This is another capturing group that matches the top-level domain (TLD), which consists of 2 to 6 lowercase letters or dots.
([\/\w \.-]*)*: This is a capturing group that matches the path part of the URL, which can contain forward slashes, alphanumeric characters, spaces, dots, and hyphens. The entire group is followed by * to allow for zero or more occurrences.
\/?: This matches an optional trailing forward slash in the URL.

### Bracket Expressions
 Bracket expressions define a character class. In this regex:

[\da-z\.-]: This character class matches any digit, lowercase letter, dot, or hyphen.

### Character Classes
Character classes represent a set of characters that can be matched. In this regex:

\d: Matches any digit (equivalent to [0-9]).

\w: Matches any word character (equivalent to [a-zA-Z0-9_]).

.: Matches a literal dot.

### The OR Operator

The OR operator (|) is not explicitly used in this regex pattern

### Flags

 Flags in regex are used to modify how the pattern is matched. They are not present in the provided regex pattern.

### Character Escapes
Character escapes are used to match specific characters that have special meanings in regex. In this regex, the backslashes \ before certain characters, like \. and \/, are used to escape them and match them literally.

## Author
Jacob Lausier