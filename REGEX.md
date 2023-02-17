# Regex 
Welcome to this tutorial on Regular Expressions! In this tutorial, I'll be breaking down a Regex to help you better understand how they work. Specifically, I'll be using a particular Regex and dissecting each part of the expression to give you a more comprehensive understanding.

### **Summary**
The regex of choice will be the email regex! it looks something like this: 
Matching an Email – /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/


### **Table of Contents**
### **Table of Contents**

* [Anchors](#anchors)
* [Quantifiers](#quantifiers)
* [OR Operator](#or-operator)
* [Character Classes](#character-classes)
* [Flags](#flags)
* [Grouping and Capturing](#grouping-and-capturing)
* [Bracket Expressions](#bracket-expressions)
* [Greedy and Lazy Match](#greedy-and-lazy-match)
* [Boundaries](#boundaries)
* [Back-references](#back-references)
* [Look-ahead and Look-behind](#look-ahead-and-look-behind)

### **Regex Components**


### **Anchors** <a name="anchors"></a>

The email regex provided above includes two anchor symbols, namely ^ and $. The caret symbol '^' is a start-of-string anchor, which indicates that the pattern must match at the beginning of the string. This ensures that the email address starts with the correct username. The dollar symbol '$' is an end-of-string anchor, which means that the pattern must match at the end of the string. This ensures that the email address ends with a valid top-level domain. Together, these two anchor symbols confirm that the email address matches the complete pattern and contains no additional characters before or after the email address

**Quantifiers**

The email regex above uses two quantifiers to specify how many times a character or set of characters should match:

The + quantifier indicates that the preceding character set should match one or more times. In this regex, it's used to match one or more occurrences of the characters in the username portion of the email address. This can include lowercase letters, numbers, underscores, periods, and dashes.

The {2,6} quantifier indicates that the preceding character set should match between 2 and 6 times. In this regex, it's used to match between 2 and 6 occurrences of lowercase letters or periods in the top-level domain portion of the email address. This ensures that the domain extension is a valid length, while also allowing for longer extensions such as .io or .tech.

**OR Operator**

In the email regex above he OR operator is represented by the pipe symbol (|) and is used to match either of two options.

In this specific regex, the OR operator is not used. However, it could be used in other regular expressions for matching email addresses, such as to allow for optional characters or variations in formatting.

For example, the regex may use the OR operator to allow for a plus sign (+) or hyphen (-) in the username portion of the email address. This would look something like: /^([a-z0-9_.-+]+)@([\da-z.-]+).([a-z.]{2,6})$/.

**Character Classes**

There are 3 main classes in the email regex, 
[a-z0-9_.-]: This character class matches any lowercase letter, digit, underscore, period, or dash in the username portion of the email address.

[\da-z.-]: This character class matches any digit, lowercase letter, period, or dash in the domain name portion of the email address.

[a-z.]: This character class matches any lowercase letter or period in the top-level domain portion of the email address. The {2,6} quantifier immediately follows this character class to ensure that the domain extension is between 2 and 6 characters long.

**Flags**

In this email regex there actually is no flags. However, flags are optional parameters in regular expressions that modify the behavior of the pattern matching. They are written after the closing delimiter of the regular expression 

**Grouping and Capturing**

Grouping and capturing in regular expressions are used to group parts of a pattern together and capture the matched values. In the email regex /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/,there are three groups, each enclosed in parentheses. The first group matches the username, the second group matches the domain name, and the third group matches the top-level domain extension. These groups allow you to extract the matched values and use them for various purposes in your code.

**Bracket Expressions**

Bracket extentions are used to define a set of characters to match a single character.

In this email regex the first group matches any lowercase letter, digit, underscore, period, or dash in the username portion of the email address. The character set [\da-z\.-] in the second group matches any digit, lowercase letter, period, or dash in the domain name. Finally, the character set [a-z\.]{2,6} in the third group matches any lowercase letter or period in the top-level domain, with a length between 2 and 6 characters.



**Greedy and Lazy Match**

The + and {2,6} quantifiers in this email regex are examples of greedy matching, where the regex engine matches as many characters as possible while still allowing the pattern to match. 

In contrast, lazy matching can be achieved by adding a ? after a quantifier, causing the engine to match as few characters as possible while still allowing the pattern to match.

**Boundaries**

In the email regex, there are two boundaries used:

The start of string boundary (^) signifies that the pattern should match at the beginning of the string. In this case, it ensures that the email address starts with the username.

The end of string boundary ($) signifies that the pattern should match at the end of the string. In this case, it ensures that the email address ends with a valid top-level domain.

Together, these boundaries ensure that the email address matches the entire pattern from start to finish and doesn't contain any extra characters before or after the email address.
Back-references

**Look-ahead and Look-behind**

Look-ahead and look-behind are zero-width assertions that allow you to match patterns based on what comes before or after a specific subpattern, without including the characters in the match itself. They are written as (?=...) for look-ahead and (?<=...) for look-behind.




## **Author**
You can find me on [github](https://github.com/RonaldMartinez00/)