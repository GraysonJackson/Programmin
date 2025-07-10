## Attributes and Methods

### Slide 1: Anatomy of a Class

  * Classes are the blueprints for objects in Object-Oriented Programming.
  * The two primary components of a class are:
      * **Attributes:** The data or state associated with an object (variables).
      * **Methods:** The behaviors or actions an object can perform (functions).

### Slide 2: Attributes

  * **Attributes** are variables that belong to an object. They define the properties of that object.
  * They are typically defined inside the `__init__()` method and are prefixed with `self.`.
  * Each instance of a class can have different values for its attributes.

<!-- end list -->
```py

class Car:
    def __init__(self, make, model, year):
        # These are the attributes
        self.make = make
        self.model = model
        self.year = year
        self.odometer_reading = 0 # An attribute with a default value
```
### Slide 3: Methods

  * **Methods** are functions that are defined inside a class. They represent the actions an object can take.
  * The first parameter of a method is always `self`, which refers to the instance calling the method. This allows the method to access the object's attributes.

<!-- end list -->
```py

class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year
        self.odometer_reading = 0

    # This is a method
    def get_descriptive_name(self):
        """Return a neatly formatted descriptive name."""
        return f"{self.year} {self.make} {self.model}"

    # Another method that modifies an attribute
    def update_odometer(self, mileage):
        """Set the odometer reading to the given value."""
        if mileage >= self.odometer_reading:
            self.odometer_reading = mileage
```
### Slide 4: Using Attributes and Methods

  * You access an object's attributes and call its methods using dot notation.

<!-- end list -->
```py

class Car:
    # (Including __init__ and methods from previous slide)
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year
        self.odometer_reading = 0
    def get_descriptive_name(self):
        return f"{self.year} {self.make} {self.model}"
    def update_odometer(self, mileage):
        if mileage >= self.odometer_reading:
            self.odometer_reading = mileage

# Create an instance
my_car = Car('Toyota', 'Corolla', 2022)

# Accessing an attribute
print(f"My car's odometer reads: {my_car.odometer_reading}")

# Calling a method
print(my_car.get_descriptive_name())

# Calling another method to change an attribute
my_car.update_odometer(150)
print(f"My car's odometer now reads: {my_car.odometer_reading}")
```
### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 17: "Classes and methods".
  * **Practice Exercise:**
      * Add a `bark()` method to the `Dog` class from the previous lesson. It should print something like "Fido says woof\!".
      * Add a `balance` attribute to a `BankAccount` class. Create `deposit()` and `withdraw()` methods that modify the balance. Make sure the `withdraw()` method doesn't allow the balance to go below zero.