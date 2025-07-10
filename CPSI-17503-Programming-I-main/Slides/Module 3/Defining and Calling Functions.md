## Defining and Calling Functions

### Slide 1: What is a Function?

  * A **function** is a named, reusable block of code that performs a specific task.
  * Functions help organize your code, make it more readable, and allow you to reuse code without rewriting it.
  * You've already used built-in functions like `print()` and `input()`.

### Slide 2: Defining a Function

  * You define a function using the `def` keyword, followed by the function name, parentheses `()`, and a colon `:`.
  * The code block within the function must be indented.

<!-- end list -->
```py

# A simple function definition
def greet():
    """This is a docstring. It explains what the function does."""
    print("Hello from a function!")
    print("Welcome.")
```
### Slide 3: Calling a Function

  * Defining a function does not execute it.
  * To run the code inside a function, you must **call** it by writing its name followed by parentheses `()`.

<!-- end list -->
```py

# Define the function
def greet():
    print("Hello from a function!")

# Call the function
print("Before the function call.")
greet()
print("After the function call.")
```
Output:

```
Before the function call.
Hello from a function!
After the function call.
```

### Slide 4: The Flow of Execution

1.  The program starts at the first line.
2.  Python reads the `def` statement and creates the function object, but does not run the code inside it.
3.  When the program reaches the function call (`greet()`), it jumps into the function.
4.  It executes all the statements inside the function.
5.  When the function ends, the program returns to the line after the function call and continues.

### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 3: "Functions".
  * **Practice Exercise:**
      * Write a function called `print_lyrics` that prints a few lines of your favorite song.
      * Call your `print_lyrics` function multiple times in your program.
      * Create a `main` function that contains the main logic of your program, and then call `main()` at the end of your script.
