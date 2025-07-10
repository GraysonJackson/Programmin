## Loops (for, while)

### Slide 1: Why Use Loops?

  * **Loops** allow you to execute a block of code repeatedly.
  * They are fundamental for automating repetitive tasks.
  * Python has two main types of loops:
      * `for` loops: Iterate over a sequence (like a list, tuple, dictionary, set, or string).
      * `while` loops: Repeat as long as a certain condition is true.

### Slide 2: The `for` Loop

  * A `for` loop is used for iterating over a sequence.
  * With each iteration, a loop variable is set to the next value in the sequence.

<!-- end list -->
```py

# Looping through a list
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)

# Looping through a string
for letter in "Python":
    print(letter)

# Using range() to loop a specific number of times
for i in range(5):  # from 0 to 4
    print(f"Iteration number {i}")
```
### Slide 3: The `while` Loop

  * A `while` loop executes a block of code as long as a condition is `True`.
  * You need to manage the loop condition yourself, often with a counter variable.
  * **Warning:** Be careful to avoid an infinite loop\! The condition must eventually become `False`.

<!-- end list -->
```py

# A simple while loop
count = 0
while count < 5:
    print(f"Count is {count}")
    count += 1  # Increment the counter. Without this, it's an infinite loop!

print("Loop finished.")
```
### Slide 4: `for` vs. `while`

  * **Use a `for` loop when:** You know how many times you want to loop (e.g., for every item in a list, for 10 repetitions). It is generally more common and less prone to infinite loop errors.
  * **Use a `while` loop when:** You want to loop until a certain condition is met (e.g., until the user enters 'quit', until a variable reaches a certain value).

### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 4: "Case study: interface design" (introduces `for` loops) and Chapter 7: "Iteration" (covers `while` loops).
  * **Practice Exercise:**
      * Use a `for` loop to print the numbers from 1 to 10.
      * Use a `while` loop to do the same thing.
      * Create a list of names. Use a `for` loop to print a greeting to each person in the list.
      * Write a simple guessing game where the program loops with a `while` loop until the user guesses the correct number.