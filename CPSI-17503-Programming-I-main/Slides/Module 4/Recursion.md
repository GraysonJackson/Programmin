## Recursion Introduction

### Slide 1: What is Recursion?

  * **Recursion** is a programming technique where a function calls itself to solve a problem.
  * It's a way of solving a problem by breaking it down into smaller, similar sub-problems.
  * A recursive function must have two parts:
    1.  A **base case**: A condition that stops the recursion.
    2.  A **recursive step**: The part of the function that calls itself.

### Slide 2: The Base Case is Crucial

  * The **base case** is the simplest version of the problem that can be solved directly, without further recursion.
  * Without a base case, a recursive function would call itself forever, leading to a "stack overflow" error.

### Slide 3: Example: Countdown

Let's write a function that counts down from a number to zero.

  * **Recursive Step:** The countdown from `n` is `n` followed by the countdown from `n-1`.
  * **Base Case:** When `n` is 0, we just say "Blastoff\!" and stop.

<!-- end list -->
```py

def countdown(n):
    # Base Case
    if n <= 0:
        print("Blastoff!")
    # Recursive Step
    else:
        print(n)
        countdown(n - 1)

# Let's try it
countdown(3)
```
**Output:**
```
3
2
1
Blastoff!
```
### Slide 4: Example: Factorial

The factorial of a number `n` (written as `n!`) is the product of all positive integers up to `n`.

  * `5! = 5 * 4 * 3 * 2 * 1`
  * **Recursive Step:** `factorial(n) = n * factorial(n-1)`
  * **Base Case:** `factorial(0) = 1`

<!-- end list -->
```py

def factorial(n):
    # Base Case
    if n == 0:
        return 1
    # Recursive Step
    else:
        return n * factorial(n - 1)

# Calculate 5!
result = factorial(5)
print(f"The factorial of 5 is {result}")  # Output: 120
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 5: "Conditionals and recursion" and Chapter 6: "Fruitful functions".
  * **Practice Exercise:**
      * Trace the execution of `factorial(3)` on paper to see how the calls are made and how the values are returned.
      * Write a recursive function `sum_to(n)` that calculates the sum of all integers from 1 to `n`. (e.g., `sum_to(3)` would be `3 + 2 + 1 = 6`). The base case is when `n` is 1.