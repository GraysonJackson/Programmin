## Selection Constructs (if, elif, else)

### Slide 1: Making Decisions in Code

  * Often, you need your program to do different things based on certain conditions.
  * **Selection constructs** allow you to control the flow of your program's execution.
  * The main selection constructs in Python are `if`, `elif`, and `else`.

### Slide 2: The `if` Statement

  * The `if` statement executes a block of code only if a condition is `True`.
  * The syntax is `if condition:`, followed by an indented block of code.

<!-- end list -->
```py

age = 20

if age >= 18:
    print("You are eligible to vote.")

print("This line runs regardless of the condition.")
```
### Slide 3: The `if-else` Statement

  * The `if-else` statement provides an alternative block of code to execute if the `if` condition is `False`.

<!-- end list -->
```py

age = 16

if age >= 18:
    print("You are eligible to vote.")
else:
    print("You are not yet eligible to vote.")
```
### Slide 4: The `if-elif-else` Chain

  * For more than two possibilities, you can use `elif` (short for "else if").
  * Python checks each condition in order. The first one that is `True` gets executed, and the rest are skipped.
  * The `else` block at the end is optional and runs if none of the preceding conditions are `True`.

<!-- end list -->
```py

score = 85

if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
elif score >= 70:
    print("Grade: C")
else:
    print("Grade: D or F")
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 5: "Conditionals and recursion".
  * **Practice Exercise:**
      * Write a program that asks for a number and prints whether the number is positive, negative, or zero.
      * Create a simple "login" program that checks if a user-entered password matches a stored password.