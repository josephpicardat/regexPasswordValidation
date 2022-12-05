# Regex Password Validation

Have you ever wondered how to black/white-list certain characters for your webisite? Well through the use of regular expression, or regex, you can do just that! In this tutorial, we will discuss how to create a way to black/white-list characters for password validation. The information in this tutorial is not just limited to password validation, but a stepping stone in learning regex.

## Summary

With the use of regilar expression, you can write the contrainsts of your desired password characters, special characters, numbers, and length for your password requirement. As the code snippet shows below, you can see the regex code required to make this happen.

                     `const password = /^(?=.*\d)(?=.*[a-z])(?=.*[A-Z])(?=.*[a-zA-Z]).{8,}$/g`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Flags](#flags)
- [Bracket Expressions](#bracket-expressions)
- [Boundaries](#boundaries)
- [Author](#author)

## Regex Components

### Anchors

Regex anchors are not made to match any characters but matches the position in the string to a specified location. For an example it can mark the start of strings or the end of a line. When we look at our code snippet for password, we can see the use of a caret `^` as the second character of the code. The caret anchor sets the current position in the string as the beginning of the string.

                        `const password = /   ^   (?=.*\d)(?=.*[a-z])(?=.*[A-Z])(?=.*[a-zA-Z]).{8,}   $   /g`

The other anchor that is used within the regex password validation is the dollar sign, `$` which marks the end of a string or line. you can write it at the end of your code like what is in this tutorial or for multiple use cases you can have it attached to a string. For example we can take the string 'racecar.' When we want to state that end of the string will be a 'r' we will write 'r$.' This only matches the ending of the string, so with the string 'racecar' only the last 'r' will register as the end. To clarify this example, the use of the string 'racecar' marks the characters chosen. So you can write, for example: 'rraacrrceccaacccccr'. As you can see the ending is an 'r,' but the contents still include the same characters as 'racecar.' If you wanted to end your character selection on 'a' or 'c,' the code will not accept it as a qualified input.

### Quantifiers

Quanitifiers indicate numbers of characters or expressions to match. These characters include:

- `*` Matches zero or more times
- `+` Matches one or more times
- `?` matches zero or one time
- `{ n }` Matches exactly n times
- `{ n , }` Matches at least n times
- `{ n , m }` Matches from n to m times

For instance in our code we have `*[a-z]` which states that it matches zero or more times from a-z characters.

### Flags

Flags allow for global searching and case-insensitive searching. Examples of these flags include:

- `d` Generate indices for substring matches
- `g` Global search
- `i` Case-insenitive search
- `m` Allows ^ and $ to match newline characters.
- `s` Allows . to match newline characters.
- `u` "Unicode"; treat a pattern as a sequence of Unicode code points.
- `y` Perform a "sticky" search that matches starting at the current position in the target string.

An example in the our code is at the end with `/g` which is a global search all characters in the code

### Bracket Expressions

Bracket expressions match or exempt a list expression of characters. We have a great example in our code `[a-z]` which tries to match everything inside of the brackets and in this case it is characters from a-z

### Boundaries

Boundaries `/b` matches the boundary of words. There are three positions that boundaries can fall under:

- Before the first character
- After the last character
- Between two characters

The example in our code is `?=.*\d` which the `.` stands for any non newline character; the `*` means it matches zero or more times and the `/d` is our boundary. Since it is at the end it sets the boundary at the end of the string.

### Author

My name is Joseph Picardat and I am software engineer. I am a professional double bass player who loves programming and trying to get into the industry.

GitHub: https://github.com/josephpicardat
