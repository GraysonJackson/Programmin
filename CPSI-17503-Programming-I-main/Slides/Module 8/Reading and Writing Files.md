## Reading and Writing Files

### Slide 1: Working with Files

  * Python can be used to read data from files and write data to files.
  * This is essential for working with data sets, logs, user-generated content, and more.
  * The basic steps are:
    1.  **Open** the file.
    2.  **Read** or **Write** to the file.
    3.  **Close** the file.

### Slide 2: Opening and Closing Files

  * The `open()` function is used to open a file. It returns a file object.
  * It takes two main arguments: the file path and the **mode**.
      * `'r'`: **Read** mode (default). Throws an error if the file doesn't exist.
      * `'w'`: **Write** mode. Creates the file if it doesn't exist, or **overwrites** the file if it does.
      * `'a'`: **Append** mode. Adds new content to the end of the file.
  * It is crucial to close the file using `file.close()` to free up system resources.

### Slide 3: The `with` Statement (Recommended)

  * The `with` statement simplifies file handling by automatically closing the file for you, even if errors occur. This is the preferred way to work with files.

<!-- end list -->
```py

# The 'with' statement ensures the file is automatically closed.
with open('example.txt', 'w') as f:
    f.write('Hello, file!\n')
    f.write('This is a second line.')

print("File has been written and closed.")
```
### Slide 4: Reading from a File

  * There are several ways to read from a file opened in read mode (`'r'`).
      * `read()`: Reads the entire content of the file into a single string.
      * `readline()`: Reads a single line from the file.
      * `readlines()`: Reads all lines into a list of strings.
      * Iterating over the file object (most common and efficient).

<!-- end list -->
```py

# Assuming 'example.txt' from the previous slide exists.
with open('example.txt', 'r') as f:
    # The best way to read line by line
    print("Reading line by line:")
    for line in f:
        print(line.strip()) # .strip() removes leading/trailing whitespace like '\n'

with open('example.txt', 'r') as f:
    # Reading the whole file at once
    content = f.read()
    print("\nReading entire file:")
    print(content)
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 14: "Files".
  * **Practice Exercise:**
      * Write a program that asks the user for their name and writes it to a file called `name.txt`.
      * Write another program that reads the name from `name.txt` and prints a greeting to the user.
      * Create a file with a list of items, one per line. Write a program to read this file and print its contents, numbered.