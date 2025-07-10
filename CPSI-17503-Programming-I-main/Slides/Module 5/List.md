## List

### Slide 1: What is a List?

  * A **list** is a collection of items that are ordered and changeable (mutable).
  * It is one of the most versatile data types in Python.
  * Lists are written with square brackets `[]`, with items separated by commas.
  * A list can contain items of different data types.

### Slide 2: Creating and Accessing Lists

  * You can create a list by putting values inside square brackets.
  * You access list items by referring to their **index number**.
  * Indexing in Python starts at **0**.

<!-- end list -->
```py

# A list of strings
fruits = ["apple", "banana", "cherry"]
print(fruits)

# A list with mixed data types
mixed_list = ["hello", 100, 3.14, True]
print(mixed_list)

# Accessing items by index
first_fruit = fruits[0]  # Get the first item
print(f"The first fruit is: {first_fruit}") # Output: apple

second_fruit = fruits[1]
print(f"The second fruit is: {second_fruit}") # Output: banana
```
### Slide 3: List Slicing

  * You can get a sub-list (a "slice") from a list by specifying a range of indices.
  * The syntax is `my_list[start:end]`.
  * The `start` index is included, but the `end` index is not.

<!-- end list -->
```py

numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

# Get numbers from index 2 up to (but not including) index 5
subset = numbers[2:5]
print(subset)  # Output: [2, 3, 4]

# Get the first three numbers
first_three = numbers[:3]
print(first_three)  # Output: [0, 1, 2]

# Get all numbers from index 6 to the end
last_part = numbers[6:]
print(last_part)  # Output: [6, 7, 8, 9]
```
### Slide 4: Lists are Mutable

  * "Mutable" means that you can change the contents of a list after it has been created.
  * You can change, add, and remove items.

<!-- end list -->
```py

colors = ["red", "green", "blue"]
print(f"Original list: {colors}")

# Change an item
colors[1] = "yellow"
print(f"After changing an item: {colors}")

# Add an item to the end
colors.append("purple")
print(f"After appending an item: {colors}")
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 10: "Lists".
  * **Practice Exercise:**
      * Create a list of your favorite movies.
      * Print the first and last movies in the list.
      * Use slicing to create a new list containing the middle movies.
      * Add a new movie to your original list and print it again to see the change.