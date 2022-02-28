# Title (replace with your title)

Regular Expressions, commonly known as regex are a tool that can be used by most programming languages to extract specific information from a block of text by searching for items that follow a specific pattern determined by the regex used. The patterns are represented by several different characters that let the system know what it should be looking for.



## Summary


We will be walking through the regex for Matching a URL. I will explain which special characters are used and what types of information they represent.

* The regex for matching a URL looks like this:

       /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

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

Anchors are represented using ^ and $ and let the system know where the string starts and ends. 
* `^` indicates the start of the string. In this code snipped, `^` is at the beginning of the URL components.
* `$` indicates the end of the string. In this code snippet, it is the final character, letting us know when it is done.


### Quantifiers

#### Quantifiers let the system know how many characters to look for.
  * `*` is a wildcard, if `*` follows a string like `yel*` then all strings starting with yel and followed by zero or more characters are found. 
   * `?` means that the prior character is optional in the search, so https? means search for http or https. (https?:\/\/)? means that the http or https might not be present anyway, and we still need to pull in results that are urls without http:// and https://
  * `+` means that we are searching for one or more of the previous character. so for [\da-z\.-]+ we are looking for at least one character, but maybe more.
  * `{2, 6}` is a way to determine what range of characters we should look for. The `{2, 6}` means we are looking for between 2 and 6 characters as the ending part of the URL.

### OR Operator

#### OR Operators tell the system to check for one option out of two or more.

  * `|` captures one type or another a|b would look for instances of either a or b.
  * `[]` all items enclosed in the brackets are part of an or statement, if of the included items are present, the criteria is met.

### Character Classes

#### Character Classes let the system know which types of characters to look for.

  * `\d` matches a single digit
  * `\w` matches an alphanumeric character or underscore.
  * `\s` matches a whitespace character (space, tab, or line break)
  * `.` matches any character. This should be used carefully.

### Grouping and Capturing

#### Grouping and capturing is used to set aside a part of the string and apply one of our other regex items to only that specific portion.

  * For instance, as we mentioned before (https?:\/\/)? means that the http or https might not be present anyway, and we still need to pull in results that are urls without http:// and https://


### Bracket Expressions

#### Bracket expressions let us know to look for one of the items within the brackets that meet the criteria.
  * `[da-z]` means to search for a digit or letter between a-z.
  * `[a-z]` means to search for a letter.

### Greedy and Lazy Match
#### Greedy and Lazy match expand the match as far as can be done through the text.
  * We use  `*` and `{}` and `+` which all count as greedy operators.


## Author

Jessica Groves is a Financial Manager turned Developer who is aiming to share resources that helped her along on her coding journey. Jessica lives in Salt Lake with her partner, toddler, and standard poodle. You can find her on [GitHub](https://github.com/jecoc0)

