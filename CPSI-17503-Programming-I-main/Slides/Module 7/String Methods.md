## String Methods

### Slide 1: What are String Methods?

  * **String methods** are built-in functions that operate on strings.
  * They allow you to perform common tasks like changing case, searching for substrings, splitting a string into a list, and more.
  * You call a method on a string using dot notation: `my_string.method_name()`.
  * **Important:** Since strings are immutable, methods do not change the original string. They **return a new modified string**.

### Slide 2: Common Formatting Methods

  * `upper()`: Returns a new string with all characters in uppercase.
  * `lower()`: Returns a new string with all characters in lowercase.
  * `capitalize()`: Returns a new string with the first character capitalized.
  * `strip()`: Returns a new string with leading and trailing whitespace removed.

<!-- end list -->
```py

message = "   Hello, World!   "
print(f"Original: '{message}'")
print(f"upper(): '{message.upper()}'")
print(f"lower(): '{message.lower()}'")
print(f"strip(): '{message.strip()}'")

original_string = "this is a title"
capitalized_string = original_string.capitalize()
print(f"capitalize(): '{capitalized_string}'")
```
### Slide 3: Searching and Replacing

  * `find(substring)`: Returns the starting index of the first occurrence of the substring. Returns -1 if not found.
  * `replace(old, new)`: Returns a new string where all occurrences of `old` are replaced with `new`.
  * `startswith(substring)`: Returns `True` if the string starts with the substring.
  * `endswith(substring)`: Returns `True` if the string ends with the substring.

<!-- end list -->
```py

sentence = "The quick brown fox jumps over the lazy dog."

print(f"Index of 'fox': {sentence.find('fox')}")
print(f"Index of 'cat': {sentence.find('cat')}")

new_sentence = sentence.replace("fox", "cat")
print(f"After replace: '{new_sentence}'")

print(f"Starts with 'The': {sentence.startswith('The')}")
```
### Slide 4: Splitting and Joining

  * `split(separator)`: Splits the string into a list of substrings based on the separator. If no separator is given, it splits by whitespace.
  * `join(iterable)`: Joins the elements of an iterable (like a list) into a single string, with the string itself as the separator.

<!-- end list -->
```py

# split()
csv_data = "apple,banana,cherry"
fruit_list = csv_data.split(',')
print(f"split(): {fruit_list}")

# join()
words = ["Python", "is", "fun"]
separator = " "
sentence = separator.join(words)
print(f"join(): '{sentence}'")
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 8: "Strings". The official Python documentation has a complete list of string methods.
  * **Practice Exercise:**
      * Take a string with extra spaces at the beginning and end, and use a method to clean it up.
      * Given a sentence, use `split()` to get a list of words, and then use a `for` loop to print each word.
      * Take a list of words and use `join()` to combine them into a single, hyphenated string (e.g., "this-is-a-string").