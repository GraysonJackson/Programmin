## Basic Program Structure

### Slide 1: The Structure of a Python Program

  * A Python program is a sequence of **statements** that are executed by the Python interpreter.
  * The simplest programs are just a series of commands in a file.
  * Python is sensitive to **indentation** (the spaces at the beginning of a line), which it uses to define blocks of code.

### Slide 2: Core Components

  * **Statements:** An instruction that the Python interpreter can execute (e.g., `print("Hello")`, `x = 5`).
  * **Comments:** Text in your code that is ignored by the interpreter but is helpful for human readers. In Python, comments start with a `#`.
  * **Functions:** Named blocks of code that perform a specific task. You can "call" a function to execute its code.
  * **Indentation:** The spaces at the beginning of a line. Python uses indentation to group statements.

### Slide 3: The "Hello, World\!" Program

This is often the first program a new programmer writes. It's a simple program that prints the text "Hello, World\!" to the screen.
```py

# This is a comment. The interpreter ignores it.

# This is a statement that calls the print() function.
print("Hello, World!")
```
### Slide 4: A Slightly More Complex Example

This program defines a function and then calls it. Notice the indentation for the code inside the function.
```py

# This is a comment explaining what the function does.
# A function definition starts with 'def'.
def greet(name):
    # The following lines are indented, so they are part of the function.
    greeting = "Hello, " + name
    print(greeting)

# This line is not indented, so it's not part of the function.
# This is where the program's execution begins.
print("Starting the program...")
greet("Alice")
print("Program finished.")

```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 1: "The way of the program" and Chapter 2: "Variables, expressions and statements".
  * **Practice Exercise:**
      * Write a Python program that has at least one comment.
      * Define a simple function that prints a message, and then call that function.
      * Experiment with indentation to see how it affects the program (and likely causes errors).
