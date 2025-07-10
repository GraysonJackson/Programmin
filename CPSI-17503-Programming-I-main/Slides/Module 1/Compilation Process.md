## Compilation Process

### Slide 1: Compilation and Interpretation

  * This slide deck explores how high-level programming languages are translated into machine-readable code.
  * The two primary methods are **compilation** and **interpretation**.

### Slide 2: The Compilation Process

  * A **compiler** translates the entire source code into machine code before the program is run.
  * The result is an executable file that can be run on a specific type of machine.
  * **Steps:**
    1.  **Source Code:** The high-level code you write.
    2.  **Compiler:** Translates the source code into object code.
    3.  **Object Code:** A low-level representation of your code.
    4.  **Linker:** Combines the object code with libraries to create an executable file.
    5.  **Executable:** A standalone program that can be run.
  * Languages like C and C++ are typically compiled.

### Slide 3: The Interpretation Process

  * An **interpreter** reads and executes the source code line by line.
  * No separate executable file is created.
  * The interpreter itself runs the program.
  * Python is an interpreted language. This is why you can type commands into a Python shell and see immediate results.

### Slide 4: Example: Python's "Compilation"

Python is often described as an interpreted language, but there's a compilation step involved. The source code is compiled into a lower-level form called **bytecode**. The Python Virtual Machine (PVM) then interprets this bytecode.
```python

# When you run this file, Python first compiles it to bytecode (.pyc file)
# Then, the Python Virtual Machine (PVM) executes the bytecode.
def greet(name):
    message = "Hello, " + name
    print(message)

greet("World")
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 1: "The way of the program".
  * **Practice Exercise:**
      * If you have a Python script, look for a `__pycache__` directory. Inside, you might find `.pyc` files, which contain the bytecode for your modules.
      * Discuss with a peer the pros and cons of compiled vs. interpreted languages (e.g., speed of execution vs. ease of development).