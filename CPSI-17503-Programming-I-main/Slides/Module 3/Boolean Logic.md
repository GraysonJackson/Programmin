## Boolean Logic

### Slide 1: Introduction to Boolean Logic

  * **Boolean logic** is a form of algebra that is centered around three simple words: "AND", "OR", and "NOT".
  * In Python, this corresponds to the `bool` data type, which can have one of two values: `True` or `False`.
  * It's the foundation of decision-making in programming.

### Slide 2: Comparison Operators

  * Comparison operators evaluate to either `True` or `False`.
  * `==` : Equal to
  * `!=` : Not equal to
  * `>` : Greater than
  * `<` : Less than
  * `>=` : Greater than or equal to
  * `<=` : Less than or equal to

### Slide 3: Logical Operators: `and`, `or`, `not`

These operators combine boolean expressions:

  * **`and`**: Returns `True` only if *both* expressions are true.
      * `True and True` is `True`
      * `True and False` is `False`
  * **`or`**: Returns `True` if *at least one* expression is true.
      * `True or False` is `True`
      * `False or False` is `False`
  * **`not`**: Inverts the boolean value.
      * `not True` is `False`

### Slide 4: Example: Using Boolean Logic

Boolean logic is most commonly used in `if` statements to control program flow.
```py

age = 25
has_license = True

# Using 'and'
if age >= 18 and has_license:
    print("You are allowed to drive.")

is_weekend = False
is_holiday = True

# Using 'or'
if is_weekend or is_holiday:
    print("You don't have to work today!")

# Using 'not'
if not is_weekend:
    print("Time to go to work.")
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 5: "Conditionals and recursion".
  * **Practice Exercise:**
      * Write a program that asks for your age and whether you are a student. Then, use boolean logic to determine if you are eligible for a student discount (e.g., age \< 25 and is a student).
      * Predict the outcome of the following expressions before running them in Python:
          * `(5 > 3) and (10 < 20)`
          * `(10 == 10) or (10 != 10)`
          * `not (5 > 10)`