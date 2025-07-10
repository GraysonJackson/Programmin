## Parameters and Arguments

### Slide 1: Making Functions More Powerful

  * Functions can be made more flexible by allowing them to accept input values.
  * **Parameters:** The variables listed inside the parentheses in the function definition. They are placeholders for the values the function will receive.
  * **Arguments:** The actual values that are passed to the function when it is called.

### Slide 2: Defining a Function with Parameters

  * You define parameters inside the parentheses of the function definition. They behave like variables inside the function.

<!-- end list -->
```py

# 'name' is a parameter of the greet function
def greet(name):
    print(f"Hello, {name}!")
```
### Slide 3: Calling a Function with Arguments

  * When you call the function, you provide the arguments in the parentheses.
  * The argument's value is assigned to the corresponding parameter.

<!-- end list -->
```py

def greet(name):
    print(f"Hello, {name}!")

# "Alice" is the argument passed to the function.
# It gets assigned to the 'name' parameter.
greet("Alice")

# "Bob" is the argument in this call.
greet("Bob")
```
### Slide 4: Multiple Parameters and Arguments

  * Functions can have multiple parameters, separated by commas.
  * When you call the function, you must provide the same number of arguments.

<!-- end list -->
```py

# This function has two parameters: 'name' and 'age'
def display_info(name, age):
    print(f"Name: {name}")
    print(f"Age: {age}")

# We call it with two arguments: "Charlie" and 25
display_info("Charlie", 25)

```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 3: "Functions".
  * **Practice Exercise:**
      * Write a function called `add_two_numbers` that takes two parameters and prints their sum.
      * Write a function `power(base, exponent)` that takes two numbers as parameters and prints the `base` raised to the power of the `exponent`. Call it with different arguments.
