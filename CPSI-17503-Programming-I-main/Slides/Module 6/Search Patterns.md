## Search Patterns

### Slide 1: What is a Search Pattern?

  * A **search pattern** is a common algorithm used to find an item in a collection (like a list or string).
  * The goal is to determine if a specific value exists within the sequence.
  * The simplest search method is a **linear search**.

### Slide 2: Linear Search

  * A **linear search** inspects each item of the collection one by one, from the beginning to the end, until the target item is found or the end of the collection is reached.
  * This is typically implemented with a `for` loop and an `if` statement.

### Slide 3: Implementing a Linear Search

Here's how to write a function that performs a linear search on a list.
```py

def linear_search(data_list, target):
    """
    Searches for a target value in a list.
    Returns True if found, False otherwise.
    """
    for item in data_list:
        # Check if the current item is the one we're looking for
        if item == target:
            print(f"Found {target}!")
            return True  # Found it! Exit the function early.

    print(f"{target} was not found.")
    return False # Went through the whole list, didn't find it.

# Example usage
numbers = [11, 23, 8, 42, 17, 9]
linear_search(numbers, 42) # Will find it
linear_search(numbers, 100) # Will not find it
```
### Slide 4: Searching with the `in` Operator

  * Python provides a much simpler and more readable way to check for the presence of an item: the `in` operator.
  * The `in` operator performs a search and returns `True` or `False`.
  * Under the hood, it works very much like the linear search loop we just wrote.

<!-- end list -->
```py

numbers = [11, 23, 8, 42, 17, 9]

# Check if 42 is in the list
if 42 in numbers:
    print("Yes, 42 is in the list.")
else:
    print("No, 42 is not in the list.")

# Check if 100 is in the list
if 100 not in numbers:
    print("Yes, 100 is not in the list.")
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 8: "Strings" (discusses traversal and the `in` operator). Searching is a fundamental concept covered in many algorithm resources.
  * **Practice Exercise:**
      * Create a list of your favorite foods.
      * Write a program that asks the user for a food and then uses the `in` operator to tell them if it's on your list.
      * (Challenge) Write a function `find_index(data_list, target)` that returns the *index* of the target if it's found, and `-1` if it's not found.