## Pattern Matching with Regex

### Slide 1: What is Regex?

  * **Regex** (or **Regular Expressions**) is a powerful tool for matching patterns in text.
  * It's a special sequence of characters that defines a search pattern.
  * You can use regex to find, validate, or replace text in very complex ways.
  * In Python, you use the built-in `re` module.
  * *Note: This is a powerful, but more advanced topic not covered in depth in the core of "Think Python".*

### Slide 2: Basic Regex Concepts

  * **Literals:** A character like `a` matches itself.
  * **Metacharacters:** Special characters with a unique meaning.
      * `.`: Matches any single character (except newline).
      * `\d`: Matches any digit (0-9).
      * `\w`: Matches any word character (letters, numbers, underscore).
      * `\s`: Matches any whitespace character (space, tab, newline).
  * **Quantifiers:** Specify how many times a character must appear.
      * `*`: Zero or more times.
      * `+`: One or more times.
      * `?`: Zero or one time.
      * `{n}`: Exactly `n` times.

### Slide 3: Using the `re` Module in Python

  * The `re` module provides several functions to work with regular expressions.
  * `re.search(pattern, string)`: Scans through a string, looking for the first location where the pattern produces a match. Returns a match object if found, otherwise `None`.
  * `re.findall(pattern, string)`: Finds all substrings where the pattern matches and returns them as a list.

### Slide 4: Example: Finding Email Addresses

Let's use regex to find all email addresses in a piece of text. A simplified email pattern could be "one or more word characters, followed by `@`, followed by more word characters, a dot, and more word characters."
```py

import re

text = "Contact us at support@example.com or for sales, sales@company.net. Do not use info@."

# A simple regex for email addresses
# \w+  -> one or more word characters
# @    -> the literal @ symbol
# \.   -> the literal . symbol
pattern = r"\w+@\w+\.\w+"

# Find all matches
emails = re.findall(pattern, text)

print(f"Found email addresses: {emails}")
# Output: ['support@example.com', 'sales@company.net']
```
### Slide 5: Further Reading and Practice

  * **Further Reading:**
      * The official Python `re` module documentation.
      * Websites like [regex101.com](https://regex101.com) are excellent for building and testing regular expressions interactively.
  * **Practice Exercise:**
      * Write a regex to find all phone numbers in the format `XXX-XXX-XXXX` in a string.
      * Write a program that uses `re.search` to validate if a user's input is a valid 5-digit zip code.