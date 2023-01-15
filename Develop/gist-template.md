# Title (replace with your title)

Regex, short for Regular Expression, is a sequence of characters used to define a specific search pattern. When seen on their own, the string of special characters look like gibberish, but the point of this tutorial is to clarify the use of the search pattern that Regex defines. When used in code, Regex can find those patterns previously mentioned and even replace a character or entire sequence within a string.

## Summary

As a creative, color unlocks an incredible realm in styling and bringing life to your page, so the example I will be using to help understand the usefulness of Regex is Hex values. Hex values refers to the hexidecimal color code, a six digit representation of RGB preceded with a `#`, that define a color being used in an application. There are two types format for the hex value, a standard one and a three digit shortand.

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

## Table of Contents

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

## Regex Components

### Anchors

Hugging either end of the Regex above, there is a `/^` and a `$/` which are known as **anchors**. 

The `/^` at the front of the expression is used to signify a string that begins with the characters that follow. This can be used to find an exact match that is case sensitive, or in this case, a range of matches defined within `[]` brackets.

The `$/` at the end of the expression is used to signift a string that ends with the characters with the preceding characters. Like the `^`, the preceding characters can be a string or a range of matches.

### Quantifiers

`{}` is the requirement for a **quantifier** of a regex used to set the amount of characters the string can have, and here we have `{6}` and `{3}` in their own curly braces. This inidicates that each bracket expression is held to that individual value. In a different kind of expression where we werent looking for two length strings, the quantifier is used to define the minimum and maximum length of a string, as so: `{3,28}`. This would indicate that the string must be `3` or more characters and `28` characters or less.
### OR Operator

The **OR Operator** is used to indicate that either component of our Regex can be used. The element used to demonstrate this is the `|` that seemingly splits our expression when in actuality it tells us that the hex code could be either the `{6}` digit format or `{3}` digit format.

### Character Classes

**Character classes** define a set of characters in which anyone can occur in a string to find a match. The `[]` brackets that surround the expression are also considered character classes. However, there character classes that specify different aspects; for example, `\d` will match a single character that is a digit and `\w` matches a word character like `[a-zA-Z0-9]`

### Flags

After the second `/` at the end of the expression, one can specify what is called a **flag**. 

`g` is for gobal which allows for the search to continue throughout the file until it has found every last match.

`i` is for a case-insensitive search which ignores "case" or capitalization when looking for a match.

`m` is for multi-line searching where a multi-line input string should be treated as multiple lines.

### Grouping and Capturing

In the case of the hex codes, we utilize the  `()` to enclose our expression which groups our double quantified pattern so that we can find both the six digit value and the three button. There are two types of groupings: **capturing** and **non-capturing**, but here, we will just be defining the capturing aspect. Capturing a group makes it possible for the sequences to be reused.

### Bracket Expressions

Briefly mentioned in the anchors section, the `[]` are what is used in order to represent the range of characters to match. These are known as **bracket expressions** that indicate the characters to include in our match. are used to define a set of characters. In our case, [a-f0-9] defines that we want to find a string that containes all the characters within the brackets, and this time the `()` are used group the two quantifiers with their string values as well. 

### Greedy and Lazy Match

**Greedy** matches try to match as many times as possible. On the opposite end, **Lazy** matches try to match as few times as possible. In our hex code example, we have a lazy match using the `?`, where as a greedy match would be indicated with a `+`.

### Boundaries

**Boundaries** is indicated with `\b` which creates a "word boundary". A word boundary is zero-length. This allows you to carry a match to the whole word using the Regex.

## Author

Victoria Mota

Victoria Mota is a mult-disciplinary creative exploring the world of code. She is currently enrolled in the Rice University Coding Bootcamp in order to receive certification in full-stack development.

Github: [v1ct0r14m](https://github.com/v1ct0r14m)
