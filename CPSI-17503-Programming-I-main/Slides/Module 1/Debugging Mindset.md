## Debugging Mindset

### Slide 1: What is Debugging?

  * **Debugging** is the process of finding and resolving defects or problems within a computer program that prevent it from operating correctly.
  * Bugs can be categorized into three main types:
      * **Syntax Errors:** The structure of your program is incorrect.
      * **Runtime Errors:** The program is syntactically correct but fails during execution.
      * **Semantic Errors:** The program runs without errors, but does not do what you intended.

### Slide 2: The Debugging Mindset

  * **Everyone makes mistakes.** Debugging is a normal part of programming.
  * **Be systematic.** Don't just change things randomly. Form a hypothesis about what is wrong and test it.
  * **Read the error message.** The error message often tells you where the problem is and what kind of error it is.
  * **Simplify the problem.** Try to create a minimal, reproducible example of the bug.
  * **Explain the problem to someone else.** Often, the act of explaining the problem will help you see the solution (this is called "rubber duck debugging").

### Slide 3: A Systematic Approach

1.  **Reproduce the bug:** Be able to reliably make the error happen.
2.  **Locate the bug:** Use `print` statements or a debugger to narrow down where the error is occurring.
3.  **Analyze the bug:** Understand why the error is happening.
4.  **Fix the bug:** Make the necessary changes to your code.
5.  **Test the fix:** Run your program again and ensure the bug is gone and you haven't introduced new bugs.

### Slide 4: Example: Debugging with `print`

A common way to debug is to print the values of variables at different points in your program to see where things go wrong.
```py

#
# This function is supposed to calculate the average of a list of numbers.
#
def calculate_average(numbers):
    total = 0
    for num in numbers:
        total += num
        print(f"Current number: {num}, current total: {total}") # Debugging print statement

    # What if the list is empty? 'len(numbers)' would be 0, causing a ZeroDivisionError.
    if len(numbers) == 0:
        return 0

    average = total / len(numbers)
    return average

# Test with an empty list
print(calculate_average([]))
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 1: "The way of the program" and Appendix A: "Debugging".
  * **Practice Exercise:**
      * Take a piece of code you've written that had a bug. Go back and see if you can identify the type of bug and how you found it.
      * Write a program that you know will have an error (e.g., dividing by zero) and read the error message carefully.