## Serialization (Pickle)

### Slide 1: What is Serialization?

  * **Serialization** is the process of converting a Python object (like a list, dictionary, or even a custom object) into a byte stream.
  * **Deserialization** is the reverse process: converting the byte stream back into a Python object.
  * This is useful for saving the state of your program to a file or sending it over a network.

### Slide 2: Python's `pickle` Module

  * Python's standard library includes the `pickle` module for easy serialization.
  * `pickle` can handle most Python objects.
  * **Warning:** The `pickle` format is specific to Python. Do not unpickle data from an untrusted source, as it can execute arbitrary code.

### Slide 3: `pickle.dump()` - Saving an Object

  * `pickle.dump(obj, file)` serializes the object `obj` and writes it to the `file` object.
  * The file must be opened in **binary write mode** (`'wb'`).

<!-- end list -->
```py

import pickle

# The Python object we want to save
my_data = {
    'name': 'Alice',
    'scores': [95, 88, 100],
    'is_active': True
}

# Open a file in binary write mode
with open('data.pkl', 'wb') as f:
    # Dump the object into the file
    pickle.dump(my_data, f)

print("Data has been pickled and saved.")
```
### Slide 4: `pickle.load()` - Loading an Object

  * `pickle.load(file)` reads a pickled object from a `file` and reconstructs it.
  * The file must be opened in **binary read mode** (`'rb'`).

<!-- end list -->
```py

import pickle

# Open the file in binary read mode
with open('data.pkl', 'rb') as f:
    # Load the data from the file
    loaded_data = pickle.load(f)

print("Data has been unpickled:")
print(loaded_data)
print(f"Type of loaded data: {type(loaded_data)}")

# You can now use the object as if it were created in the program
print(f"Name: {loaded_data['name']}")
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 14 mentions "pickling". The official Python `pickle` module documentation is the best source for details.
  * **Practice Exercise:**
      * Create a list of lists (e.g., a small spreadsheet of data).
      * Use `pickle` to save this list to a file.
      * Write another script that loads the data from the file and prints one of the inner lists.