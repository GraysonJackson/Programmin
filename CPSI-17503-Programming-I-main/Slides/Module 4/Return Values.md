## Return Values

### Slide 1: Getting Output from Functions

  * So far, our functions have only printed output to the screen.
  * A function can also **return** a value to whoever called it. This allows you to use the result of a function's calculation in other parts of your code.
  * The `return` statement is used to send a value back from a function.

### Slide 2: The `return` Statement

  * When a `return` statement is executed, the function immediately stops and sends the specified value back.
  * The value that is returned can be stored in a variable.

<!-- end list -->
```py

def add(a, b):
    # This function calculates the sum and returns it
    total = a + b
    return total

# Call the function and store the result in a variable
sum_result = add(5, 3)

print(f"The result is: {sum_result}")
print(f"We can use the result in other calculations: {sum_result * 2}")
```
### Slide 3: `return` vs. `print`

  * `print()` displays a value on the screen for a human to see. It does not give a value back to the program.
  * `return` sends a value back to the code that called the function. This value can be used in further computations. A function that returns a value is sometimes called a "fruitful function".

### Slide 4: Functions without an Explicit `return`

  * If a function does not have a `return` statement, it automatically returns a special value called `None`.
  * `None` represents the absence of a value.

<!-- end list -->
```py

def greet(name):
    print(f"Hello, {name}")

result = greet("Alice")
print(f"The return value of greet is: {result}")
# Output will be:
# Hello, Alice
# The return value of greet is: None
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 6: "Fruitful functions".
  * **Practice Exercise:**
      * Write a function `multiply(x, y)` that takes two numbers and *returns* their product. Store the result in a variable and print it.
      * Create a function `is_even(number)` that returns `True` if a number is even and `False` otherwise. Use the result of this function in an `if` statement.
