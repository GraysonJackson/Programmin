## Scope

### Slide 1: What is Variable Scope?

  * **Scope** refers to the region of a program where a variable can be accessed.
  * Not all variables are accessible from all parts of our program.
  * Python has two main types of scope:
      * **Local Scope**
      * **Global Scope**

### Slide 2: Local Scope

  * A variable created **inside a function** belongs to the *local scope* of that function.
  * It can only be used inside that function.
  * It is created when the function is called and destroyed when the function returns.

<!-- end list -->
```py

def my_function():
    # 'x' is a local variable
    x = 10
    print("Inside the function, x =", x)

my_function()

# This would cause an error because 'x' is not defined in the global scope
# print("Outside the function, x =", x)
```
### Slide 3: Global Scope

  * A variable created in the main body of a Python script is a **global variable** and belongs to the *global scope*.
  * Global variables can be accessed from any scope (global and local).

<!-- end list -->
```py

# 'y' is a global variable
y = 20

def another_function():
    # We can access the global variable 'y' from inside the function
    print("Inside the function, y =", y)

another_function()
print("Outside the function, y =", y)
```
### Slide 4: The `global` Keyword

  * If you need to *modify* a global variable from inside a function, you must use the `global` keyword.

<!-- end list -->
```py

z = 30

def modify_global():
    # Use the 'global' keyword to indicate we want to change the global 'z'
    global z
    z = 100
    print("Inside the function, z =", z)

print("Before function call, z =", z)
modify_global()
print("After function call, z =", z)
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 3: "Functions" (see section on variables and parameters) and Chapter 6 (for more on how scope affects function results).
  * **Practice Exercise:**
      * Write a program with a global variable and a function. Inside the function, try to print the global variable.
      * Create a function that defines a local variable. Try to print that variable outside the function and observe the `NameError`.
      * Write a function that uses the `global` keyword to modify a global variable.