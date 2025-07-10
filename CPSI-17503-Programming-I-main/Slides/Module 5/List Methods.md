## List Methods (Stacks/Queues)

### Slide 1: Modifying Lists with Methods

  * Lists come with built-in **methods**, which are like functions that belong to the list object.
  * These methods allow you to easily modify the list, such as adding, removing, or reordering elements.
  * You call a method using dot notation: `my_list.method_name()`.

### Slide 2: Common List Methods

  * `append(item)`: Adds an item to the end of the list.
  * `insert(index, item)`: Inserts an item at a specific position.
  * `pop(index)`: Removes the item at a specific position and returns it. If no index is specified, it removes and returns the last item.
  * `remove(item)`: Removes the first occurrence of a specific item.
  * `sort()`: Sorts the list in place.
  * `reverse()`: Reverses the order of elements in the list in place.

### Slide 3: Example: Using List Methods
```py

my_list = [3, 1, 4]
print(f"Original: {my_list}")

my_list.append(2)
print(f"After append(2): {my_list}")

my_list.insert(0, 5)
print(f"After insert(0, 5): {my_list}")

my_list.sort()
print(f"After sort(): {my_list}")

removed_item = my_list.pop(2)
print(f"After pop(2): {my_list}, removed item: {removed_item}")
```
## Slide 4: Lists as Stacks (LIFO)

  * A **stack** is a data structure that follows the "Last-In, First-Out" (LIFO) principle. Think of a stack of plates.
  * You can easily use a list as a stack with the `append()` and `pop()` methods.
      * `append()` is "pushing" an item onto the stack.
      * `pop()` (with no index) is "popping" an item off the stack.

<!-- end list -->
```py

stack = []
stack.append('A')  # Push 'A'
stack.append('B')  # Push 'B'
stack.append('C')  # Push 'C'
print(f"Stack: {stack}")

item = stack.pop() # Pop the last item ('C')
print(f"Popped: {item}, Stack is now: {stack}")
```
### Slide 5: Lists as Queues (FIFO)

  * A **queue** is a data structure that follows the "First-In, First-Out" (FIFO) principle. Think of a line at a checkout counter.
  * Using a list as a queue is less efficient, but possible.
      * `append()` is "enqueuing" (joining the line).
      * `pop(0)` is "dequeuing" (the first person leaves the line).

<!-- end list -->
```py

queue = []
queue.append('First')   # 'First' joins the queue
queue.append('Second')  # 'Second' joins
queue.append('Third')   # 'Third' joins
print(f"Queue: {queue}")

item = queue.pop(0)     # The first item ('First') leaves
print(f"Served: {item}, Queue is now: {queue}")
```
*(Note: For serious queue implementation, `collections.deque` is more efficient.)*

### Slide 6: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 10: "Lists". The official Python documentation on data structures also has a great section on this.
  * **Practice Exercise:**
      * Create a to-do list. Use `append()` to add tasks. Use `pop()` to remove and complete tasks.
      * Simulate a short line of people waiting for a bus using a list as a queue.