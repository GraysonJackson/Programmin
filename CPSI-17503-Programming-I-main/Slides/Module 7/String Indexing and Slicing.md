## String Indexing and Slicing

### Slide 1: Strings as Sequences

  * In Python, a **string** is a sequence of characters.
  * Because it's a sequence, you can access its parts using **indexing** and **slicing**, just like with lists.
  * Remember that strings are **immutable**, so you can't change them in place.

### Slide 2: String Indexing

  * You can access individual characters in a string using their index in square brackets `[]`.
  * **Positive Indexing:** Starts from 0 for the first character.
  * **Negative Indexing:** Starts from -1 for the last character.

<!-- end list -->
```py

my_string = "Python"

# Positive Indexing
first_char = my_string[0]  # 'P'
second_char = my_string[1] # 'y'
print(f"First character: {first_char}")

# Negative Indexing
last_char = my_string[-1] # 'n'
second_last_char = my_string[-2] # 'o'
print(f"Last character: {last_char}")
```
### Slide 3: String Slicing

  * **Slicing** allows you to get a substring from a string.
  * The syntax is `my_string[start:stop:step]`.
      * `start`: The index where the slice begins (inclusive). Defaults to 0.
      * `stop`: The index where the slice ends (exclusive). Defaults to the end of the string.
      * `step`: The amount to increment by. Defaults to 1.

<!-- end list -->
```py

my_string = "Hello, World!"

# Slice from index 7 to 11
substring1 = my_string[7:12]
print(substring1) # Output: World

# Slice from the beginning to index 4
substring2 = my_string[:5]
print(substring2) # Output: Hello

# Slice from index 7 to the end
substring3 = my_string[7:]
print(substring3) # Output: World!
```
### Slide 4: Advanced Slicing with `step`

  * The `step` argument lets you take every Nth character. A negative step reverses the string.

<!-- end list -->
```py

my_string = "0123456789"

# Get every second character
every_other = my_string[::2]
print(every_other) # Output: 02468

# Reverse the string with a negative step
reversed_string = my_string[::-1]
print(reversed_string) # Output: 9876543210
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 8: "Strings".
  * **Practice Exercise:**
      * Given the string `s = "Programming"`, write code to get:
          * The first character.
          * The last character.
          * The substring "gram".
          * The string reversed.
      * Write a function that takes a string and returns `True` if it's a palindrome (reads the same forwards and backwards). Hint: Slicing is very useful here\!