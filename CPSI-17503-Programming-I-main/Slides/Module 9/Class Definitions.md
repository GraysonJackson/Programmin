## Class Definitions

### Slide 1: Introduction to Object-Oriented Programming (OOP)

  * **Object-Oriented Programming (OOP)** is a programming paradigm based on the concept of "objects".
  * Objects can contain data (in the form of fields, often known as **attributes**) and code (in the form of procedures, often known as **methods**).
  * A **class** is a blueprint for creating objects.

### Slide 2: What is a Class?

  * A **class** is a template or blueprint for creating objects. It defines the properties (attributes) and behaviors (methods) that all objects of that class will have.
  * Think of a `Dog` class as the blueprint for all dogs. Each individual dog (like Fido or Rover) is an **instance** or **object** of the `Dog` class.

### Slide 3: Defining a Class in Python

  * You define a class using the `class` keyword, followed by the class name (in `PascalCase`) and a colon.
  * The `__init__()` method is a special method called a **constructor**. It's called automatically when you create a new object from the class.
  * `self` represents the instance of the class. It's used to access variables that belong to the class.

<!-- end list -->
```py

class Dog:
    # The constructor method
    def __init__(self, name, age):
        # These are attributes of the Dog object
        self.name = name
        self.age = age
        print(f"A new dog named {self.name} has been created!")

# This is how you create an object (an instance) of the Dog class
my_dog = Dog("Fido", 5)
another_dog = Dog("Rover", 2)
```
### Slide 4: Creating Instances (Objects)

  * Once you have a class definition, you can create multiple **instances** (objects) from it.
  * Each instance is a distinct object with its own set of attributes.

<!-- end list -->
```py

class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

# Create two different Dog objects
dog1 = Dog("Fido", 5)
dog2 = Dog("Rover", 2)

# Each object has its own data
print(f"{dog1.name} is {dog1.age} years old.") # Output: Fido is 5 years old.
print(f"{dog2.name} is {dog2.age} years old.") # Output: Rover is 2 years old.
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 15: "Classes and objects", Chapter 16: "Classes and functions", and Chapter 17: "Classes and methods".
  * **Practice Exercise:**
      * Define a `Car` class.
      * The `__init__` method should take `make`, `model`, and `year` as arguments and store them as attributes.
      * Create two different `Car` objects with different makes and models.
      * Print out the attributes of each car object you created.