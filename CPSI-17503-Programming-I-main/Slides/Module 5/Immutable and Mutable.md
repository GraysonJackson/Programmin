## Immutable/Mutable (Tuple)

### Slide 1: Mutable vs. Immutable Objects

  * In Python, data types can be classified as either **mutable** or **immutable**.
  * **Mutable:** The object's state or contents can be changed after it is created.
      * Example: `list`, `dict`
  * **Immutable:** The object's state cannot be changed after it is created.
      * Example: `int`, `float`, `str`, `bool`, `tuple`

### Slide 2: Mutable Example: Lists

  * Lists are **mutable**. You can change individual elements, add new ones, or remove them. This modifies the original list object.

<!-- end list -->
```py

# A list is mutable
my_list = [1, 2, 3]
print(f"Original list: {my_list}, ID: {id(my_list)}")

# Modify the list
my_list[0] = 99
my_list.append(4)

print(f"Modified list: {my_list}, ID: {id(my_list)}")
# The ID remains the same, proving the object itself was changed.
```
### Slide 3: Immutable Example: Strings

  * Strings are **immutable**. You cannot change a character within a string. Any operation that looks like a modification actually creates a *new* string object.

<!-- end list -->
```py

# A string is immutable
my_string = "hello"
print(f"Original string: {my_string}, ID: {id(my_string)}")

# This will cause an error:
# my_string[0] = 'H' # TypeError: 'str' object does not support item assignment

# Operations like this create a NEW string
my_string = my_string + " world"
print(f"New string: {my_string}, ID: {id(my_string)}")
# The ID is now different, proving it's a new object.
```
### Slide 4: Introduction to Tuples

  * A **tuple** is an ordered collection of items, similar to a list.
  * The key difference is that tuples are **immutable**. Once a tuple is created, you cannot change its contents.
  * Tuples are defined using parentheses `()`.

<!-- end list -->
```py

# A tuple of numbers
my_tuple = (1, 2, 3)
print(my_tuple)

# Accessing elements is the same as with lists
print(f"First element: {my_tuple[0]}")

# This would cause a TypeError:
# my_tuple[0] = 99

```
### Slide 5: When to Use Tuples

  * Use tuples when you have a collection of items that should not change, such as coordinates, RGB color values, or days of the week.
  * They can be used as keys in a dictionary (lists cannot).
  * They are generally slightly more memory-efficient and faster to process than lists.

### Slide 6: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 12: "Tuples".
  * **Practice Exercise:**
      * Create a tuple to store the RGB values for the color red: `(255, 0, 0)`. Try to change one of the values and observe the error.
      * Create a list and a tuple, each with the same elements. Use the `id()` function to see their memory addresses before and after trying to modify them.
      * Write a function that returns multiple values (e.g., `return x, y`). Observe that the function actually returns a tuple.