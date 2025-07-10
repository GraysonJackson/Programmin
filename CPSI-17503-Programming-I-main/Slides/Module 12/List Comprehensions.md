## List Comprehensions

### Slide 1: What are List Comprehensions?

  * **List comprehensions** provide a concise and readable way to create lists in Python.
  * They allow you to generate a new list by applying an expression to each item in an existing sequence (like a list, tuple, or range).
  * The syntax can be easier to read than a traditional `for` loop for creating lists.

### Slide 2: The Basic Syntax

  * A list comprehension consists of brackets containing an expression followed by a `for` clause.
  * Basic syntax: `[expression for item in iterable]`

**Traditional `for` loop:**
```py

squares = []
for x in range(10):
    squares.append(x**2)
print(squares) # Output: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```
**Equivalent list comprehension:**
```py

squares = [x**2 for x in range(10)]
print(squares) # Output: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```
### Slide 3: Adding a Conditional Filter

  * You can add an `if` condition to the end of a list comprehension to filter the items from the original sequence.
  * Syntax: `[expression for item in iterable if condition]`

**Traditional `for` loop:**
```py

even_squares = []
for x in range(10):
    if x % 2 == 0:
        even_squares.append(x**2)
print(even_squares) # Output: [0, 4, 16, 36, 64]
```
**Equivalent list comprehension:**
```py

even_squares = [x**2 for x in range(10) if x % 2 == 0]
print(even_squares) # Output: [0, 4, 16, 36, 64]
```
### Slide 4: More Examples

List comprehensions can work with any iterable and can use complex expressions.
```py

# Create a list of uppercase names from an existing list
names = ["alice", "bob", "charlie"]
upper_names = [name.upper() for name in names]
print(upper_names) # Output: ['ALICE', 'BOB', 'CHARLIE']

# Get the length of each word
words = ["hello", "world", "in", "python"]
lengths = [len(word) for word in words]
print(lengths) # Output: [5, 5, 2, 6]
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 19: "The Goodies" discusses list comprehensions. The official Python documentation tutorial also has a great section.
  * **Practice Exercise:**
      * Use a list comprehension to create a list of the first 10 multiples of 3 (3, 6, 9, ...).
      * Given a list of numbers `nums = [1, -2, 3, -4, 5]`, use a list comprehension to create a new list containing only the positive numbers.
      * Given a list of words, create a new list containing only the words that have more than 4 letters.