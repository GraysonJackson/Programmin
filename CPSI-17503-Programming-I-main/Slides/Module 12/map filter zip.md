## map, filter, zip

### Slide 1: Functional Programming Tools

  * Python offers several built-in functions that are common in functional programming.
  * `map()`, `filter()`, and `zip()` allow you to process iterables (like lists) in a concise and efficient way.
  * These functions return **iterators**, which are memory-efficient objects that you can loop over or convert to a list.

### Slide 2: `map()`

  * `map(function, iterable)` applies a given `function` to every item of an `iterable` and returns a map object (an iterator) of the results.

**Traditional `for` loop:**
```py

numbers = [1, 2, 3, 4]
squared = []
for num in numbers:
    squared.append(num**2)
```
**Using `map()`:**
```py

numbers = [1, 2, 3, 4]
def square(n):
    return n**2

# map() returns an iterator, so we convert it to a list to see the results
squared = list(map(square, numbers))
print(squared) # Output: [1, 4, 9, 16]
```
### Slide 3: `filter()`

  * `filter(function, iterable)` filters elements from an `iterable`, returning only the items for which the `function` returns `True`.

**Traditional `for` loop:**
```py

numbers = [1, 2, 3, 4, 5, 6]
evens = []
for num in numbers:
    if num % 2 == 0:
        evens.append(num)
```
**Using `filter()`:**
```py

numbers = [1, 2, 3, 4, 5, 6]
def is_even(n):
    return n % 2 == 0

# filter() also returns an iterator
evens = list(filter(is_even, numbers))
print(evens) # Output: [2, 4, 6]
```
### Slide 4: `zip()`

  * `zip(*iterables)` takes one or more iterables and aggregates them into a single iterator of tuples. The i-th tuple contains the i-th element from each of the argument iterables.
  * It stops when the shortest input iterable is exhausted.

<!-- end list -->
```py

names = ["Alice", "Bob", "Charlie"]
ages = [25, 30, 35]
cities = ["New York", "London", "Paris"]

# Zip them together
combined = zip(names, ages, cities)

# Convert the iterator to a list to see the tuples
print(list(combined))
# Output: [('Alice', 25, 'New York'), ('Bob', 30, 'London'), ('Charlie', 35, 'Paris')]

# You can easily loop through the zipped data
for name, age, city in zip(names, ages, cities):
    print(f"{name} is {age} years old and lives in {city}.")
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 12: "Tuples" discusses `zip`. The official Python documentation for `map`, `filter`, and `zip` is excellent.
  * **Practice Exercise:**
      * Use `map()` and a `lambda` function to convert a list of temperatures in Celsius to Fahrenheit. `F = C * 9/5 + 32`.
      * Use `filter()` to get a list of words from a sentence that are longer than 5 letters.
      * You have a list of products and a list of prices. Use `zip()` to create a list of `(product, price)` tuples.