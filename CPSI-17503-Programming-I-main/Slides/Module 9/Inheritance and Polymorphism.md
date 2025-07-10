## Inheritance and Polymorphism

### Slide 1: Inheritance: Creating Specialized Classes

  * **Inheritance** is a fundamental concept in OOP where a new class (the **child** or **subclass**) can inherit attributes and methods from an existing class (the **parent** or **superclass**).
  * This promotes code reuse and creates a logical hierarchy.
  * The child class can use all the parent's functionality and can also add its own new features or override existing ones.
  * This represents an "is-a" relationship (e.g., a `Dog` is an `Animal`).

### Slide 2: Implementing Inheritance

  * To create a child class, you put the parent class's name in parentheses after the child class name.
  * The `super()` function is used to call methods from the parent class, which is especially useful for calling the parent's `__init__()` method.

<!-- end list -->
```py

# Parent Class
class Animal:
    def __init__(self, name):
        self.name = name
    def speak(self):
        print("Some generic animal sound")

# Child Class
class Dog(Animal): # Dog inherits from Animal
    def __init__(self, name, breed):
        super().__init__(name) # Call the parent's constructor
        self.breed = breed

    # Overriding the parent's speak method
    def speak(self):
        print("Woof!")

# Create instances
generic_animal = Animal("Creature")
my_dog = Dog("Fido", "Golden Retriever")

generic_animal.speak() # Output: Some generic animal sound
my_dog.speak()         # Output: Woof!
print(f"{my_dog.name} is a {my_dog.breed}") # Can access attributes from both classes
```
### Slide 3: Polymorphism: Many Forms

  * **Polymorphism** (from Greek, meaning "many forms") is the ability of different objects to respond to the same method call in different ways.
  * In the previous example, both `Animal` and `Dog` objects have a `speak()` method. When you call `speak()` on an object, Python automatically calls the correct version for that object's class.
  * This allows you to write flexible code that can work with objects of different but related types.

### Slide 4: Example of Polymorphism

We can write a function that works with any object that has a `speak()` method, without needing to know its specific class.
```py

class Cat(Animal): # Another child of Animal
    def speak(self):
        print("Meow")

# Create a list of different but related objects
animals = [Dog("Fido", "Retriever"), Cat("Whiskers"), Animal("Generic")]

# This loop demonstrates polymorphism
for animal in animals:
    # We don't care if it's a Dog, Cat, or Animal.
    # We just know it can .speak().
    print(f"{animal.name} says:", end=" ")
    animal.speak()
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 18: "Inheritance".
  * **Practice Exercise:**
      * Create a parent class `Vehicle` with attributes like `make` and `model`.
      * Create two child classes, `Car` and `Motorcycle`, that inherit from `Vehicle`.
      * Give the `Car` class a `num_doors` attribute and the `Motorcycle` class a `has_sidecar` attribute.
      * Create a common method in `Vehicle` called `display_info()` and override it in the child classes to display their specific information.