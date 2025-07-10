## Conditional Expressions

### Slide 1: What are Conditional Expressions?

  * A **conditional expression** (also known as a **ternary operator**) is a concise way to write a simple `if/else` statement in a single line.
  * It allows you to choose a value based on a condition.
  * It is used for assigning a value to a variable, not for controlling the flow of execution of large blocks of code.

### Slide 2: The Syntax

  * The syntax is different from a standard `if/else` block and reads more like a sentence.
  * Syntax: `value_if_true if condition else value_if_false`

**Traditional `if/else` block:**
```py

age = 20
if age >= 18:
    status = "Adult"
else:
    status = "Minor"
print(status) # Output: Adult
```
**Equivalent conditional expression:**
```py

age = 20
status = "Adult" if age >= 18 else "Minor"
print(status) # Output: Adult
```
### Slide 3: When to Use Conditional Expressions

  * Conditional expressions are best used for short, simple assignments where an `if/else` block would be unnecessarily long.
  * They improve conciseness and can sometimes make code more readable, if not overused.
  * **Avoid using them for complex logic or nested conditions**, as this can quickly make the code difficult to understand.

### Slide 4: Example: Pluralization

Conditional expressions are great for simple logical choices, like choosing between a singular and plural noun.
```py
num_items = 1
# Using a conditional expression to choose the correct word
item_word = "item" if num_items == 1 else "items"
print(f"You have {num_items} {item_word}.") # Output: You have 1 item.

num_items = 5
item_word = "item" if num_items == 1 else "items"
print(f"You have {num_items} {item_word}.") # Output: You have 5 items.
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 19: "The Goodies" touches on conditional expressions. Many Python style guides offer advice on when and when not to use them.
  * **Practice Exercise:**
      * Write a program that sets a variable `is_weekend` to `True` or `False`. Use a conditional expression to set a `message` variable to either "Time to relax\!" or "Time to work\!".
      * Given a variable `score`, use a conditional expression to assign the string "Pass" or "Fail" to a `result` variable. The passing score is 60.