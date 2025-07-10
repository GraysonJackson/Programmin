## Arithmetic and Logical Operations

### Slide 1: Operations in Python

  * Python provides operators to perform calculations and logical comparisons.
  * **Arithmetic Operators:** For mathematical calculations.
  * **Logical Operators:** For combining boolean values.

### Slide 2: Arithmetic Operators

These operators work on numbers (`int` and `float`).

  * `+` : Addition
  * `-` : Subtraction
  * `*` : Multiplication
  * `/` : Division (results in a float)
  * `//` : Floor Division (discards the fractional part)
  * `%` : Modulo (returns the remainder of a division)
  * `**` : Exponentiation (raise to the power of)

### Slide 3: Example: Arithmetic Operators
```py

a = 10
b = 3

print(f"a + b = {a + b}")    # Output: 13
print(f"a - b = {a - b}")    # Output: 7
print(f"a * b = {a * b}")    # Output: 30
print(f"a / b = {a / b}")    # Output: 3.333...
print(f"a // b = {a // b}")  # Output: 3
print(f"a % b = {a % b}")    # Output: 1
print(f"a ** b = {a ** b}")  # Output: 1000
```
### Slide 4: Logical Operators

These operators work on boolean values (`True` and `False`).

  * `and`: `True` if both operands are true.
  * `or`: `True` if at least one operand is true.
  * `not`: Inverts the boolean value (`True` becomes `False`, `False` becomes `True`).

### Slide 5: Example: Logical Operators
```py

x = True
y = False

# and operator
print(f"x and y is {x and y}")  # Output: False
print(f"x and x is {x and x}")  # Output: True

# or operator
print(f"x or y is {x or y}")    # Output: True

# not operator
print(f"not x is {not x}")      # Output: False
```
### Slide 6: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 2: "Variables, expressions and statements" and Chapter 5: "Conditionals and recursion".
  * **Practice Exercise:**
      * Write a program that takes two numbers as input and prints the results of all the arithmetic operations on them.
      * Write a program that demonstrates the use of logical operators with `if` statements (e.g., `if age > 18 and has_license:`).
