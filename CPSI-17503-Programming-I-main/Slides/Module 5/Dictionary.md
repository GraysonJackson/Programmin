## Dictionary

### Slide 1: What is a Dictionary?

  * A **dictionary** is a collection that is unordered, changeable (mutable), and indexed by **keys**.
  * It stores data in **key-value pairs**.
  * Dictionaries are written with curly braces `{}`, and they have keys and values.
  * Think of it like a real dictionary: you look up a word (the key) to find its definition (the value).

### Slide 2: Creating and Accessing Dictionaries

  * Each key is separated from its value by a colon `:`, and the pairs are separated by commas.
  * You access the value by referring to its key inside square brackets `[]`.

<!-- end list -->
```py

# Creating a dictionary
student = {
    "name": "Alice",
    "age": 21,
    "major": "Computer Science"
}

print(student)

# Accessing a value by its key
student_name = student["name"]
print(f"Student's name is: {student_name}")

# Using the .get() method is safer (avoids errors for missing keys)
student_grade = student.get("grade", "N/A") # Provides a default value
print(f"Student's grade is: {student_grade}")
```
### Slide 3: Modifying a Dictionary

  * Dictionaries are mutable, so you can add, change, and remove key-value pairs.

<!-- end list -->
```py

# Starting with our student dictionary
student = { "name": "Alice", "age": 21 }
print(f"Original: {student}")

# Changing a value
student["age"] = 22
print(f"After age change: {student}")

# Adding a new key-value pair
student["grade"] = "A"
print(f"After adding grade: {student}")

# Removing a key-value pair
del student["age"]
print(f"After deleting age: {student}")
```
### Slide 4: Looping Through a Dictionary

  * You can loop through a dictionary to access its keys, values, or both.

<!-- end list -->
```py

student = { "name": "Alice", "major": "CompSci", "year": 2 }

# Loop through keys (this is the default)
print("\nKeys:")
for key in student:
    print(key)

# Loop through values
print("\nValues:")
for value in student.values():
    print(value)

# Loop through key-value pairs
print("\nItems:")
for key, value in student.items():
    print(f"{key}: {value}")
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 11: "Dictionaries".
  * **Practice Exercise:**
      * Create a dictionary to store information about your favorite book (title, author, year published).
      * Print out the author of the book.
      * Add a new key-value pair for the genre of the book.
      * Loop through the dictionary and print each piece of information on a new line, like "title: The Hobbit".