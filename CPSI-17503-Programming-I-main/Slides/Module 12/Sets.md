## Sets

### Slide 1: What is a Set?

  * A **set** is an unordered collection of **unique** elements.
  * "Unordered" means that the items do not have a defined order; you cannot refer to them by index.
  * "Unique" means that a set cannot contain duplicate elements.
  * Sets are mutable (you can add or remove elements).
  * They are written with curly braces `{}` or created with the `set()` function.

### Slide 2: Creating Sets and Key Properties

  * Sets automatically handle uniqueness.
  * To create an empty set, you must use `set()`, as `{}` creates an empty dictionary.

<!-- end list -->
```py

# Creating a set from a list - duplicates are automatically removed
numbers = [1, 2, 2, 3, 4, 4, 4]
unique_numbers = set(numbers)
print(unique_numbers) # Output: {1, 2, 3, 4}

# Creating a set with curly braces
fruits = {"apple", "banana", "cherry"}
print(fruits)

# Adding an element that already exists does nothing
fruits.add("apple")
print(fruits) # Output: {'cherry', 'apple', 'banana'} (order may vary)
```
### Slide 3: Set Operations

  * Sets are powerful because they support mathematical set operations.
  * `union (|)`: Returns a new set with all elements from both sets.
  * `intersection (&)`: Returns a new set with only the elements that are in both sets.
  * `difference (-)`: Returns a new set with elements in the first set but not in the second.
  * `symmetric_difference (^)`: Returns a new set with elements in either set, but not both.

### Slide 4: Example: Set Operations
```py

set_a = {1, 2, 3, 4}
set_b = {3, 4, 5, 6}

# Union: all unique elements from both
print(f"Union: {set_a | set_b}") # Output: {1, 2, 3, 4, 5, 6}

# Intersection: only elements in both
print(f"Intersection: {set_a & set_b}") # Output: {3, 4}

# Difference: elements in A but not in B
print(f"Difference (A - B): {set_a - set_b}") # Output: {1, 2}

# Symmetric Difference: elements in one set or the other, but not both
print(f"Symmetric Difference: {set_a ^ set_b}") # Output: {1, 2, 5, 6}
```
### Slide 5: When to Use Sets

  * **Removing duplicates:** Quickly get the unique items from a list.
  * **Membership testing:** Checking if an item exists in a collection is very fast with sets (much faster than lists).
  * **Set math:** When you need to find unions, intersections, or differences between two collections.

### Slide 6: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 19: "The Goodies" discusses sets. The official Python documentation on Set Types is also very detailed.
  * **Practice Exercise:**
      * Create two lists of names, `class1` and `class2`, with some overlapping names.
      * Convert these lists to sets.
      * Use set operations to find:
          * All students in both classes combined.
          * Students who are in both classes.
          * Students who are only in `class1`.