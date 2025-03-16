# Strings in Python

In Python if you want to type or store alphanumeric values in a variable or another object like a list or array you will use the _string_ data type as it is the preferred data type for storing a series of characters.

> Anything that is written between two single or double quotes will be considered as a string in Python.

## Letter-casing
Python contains many different built-in methods that are for the string data type and make working with strings easier.

The `title()` methods will capitalize the first letter and make all other letters lowercase of any string that is passed into it and make the text look like a title. The words _Hello_, _hello_, and _HELLO_ will all be transformed into _Hello_ when passed through the `title()` method in Python.

The `upper()` and `lower()` methods will make all the characters of the strings that are passed into them uppercase or lowercase respectively.
## F-strings
Everything between two double or single quotes will be considered as a string in python but if we want to make our string dynamic we can insert a variable into our string so the value of the variable will become a part of our string.

> This is done using format strings or `f-strings` for short, f strings allow us to insert variables inside strings.

```python
name = Harry
message = print(f"Hello, {name}")
```

F-strings can be used in multiple places where you need to update a part of a string such as welcoming the user after they login or display the number of active users on a website.

## Trimming Whitespace

Whitespace in programming means inserting spaces between characters or the end-of-line characters and even newlines are considered as whitespace. In python, whitespaces allow you to format your output to be more readable.

- Adding a `\t` before a string will insert a tab that's about four to five spaces before the string is printed on the console.
- Adding a `\n` will start each separate character in a newline.

> You can also combine newlines and tabs to better format your output.

Whitespace is great for formatting the output of your programs to make them more easier for the user to understand but adding unnecessary whitespace in your code can lead to bugs and errors. Stripping away whitespace from user input is also a common thing that most programs do since a space is a separate character.

> If a user enters their password and mistypes an extra space or tab then the password would be incorrect.

The `strip()` method in Python removes any kind of whitespace in a string and the `rstrip()` and `lstrip()` methods remove whitespaces from the right and left side of the string respectively.

## Prefixes and Suffiexs
A lot of times you could be working on a program where the user has to input a value that has a prefix or suffix. A URL for example has the http:// as a prefix and the domain like .com or .org as a suffix.

> These values can be removed by using the `removeprefix()` and `removesuffix()` methods respectively.

## Related Notes