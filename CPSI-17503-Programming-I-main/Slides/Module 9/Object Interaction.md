## Object Interaction

### Slide 1: Objects Working Together

  * In real-world applications, programs are made of multiple objects that interact with each other.
  * **Object interaction** is when one object holds a reference to another object or calls another object's methods.
  * This allows you to model more complex systems.

### Slide 2: Objects as Attributes

  * A common form of interaction is when one object is an attribute of another. This is known as **composition**.
  * For example, a `Car` object might have an `Engine` object as one of its attributes.

<!-- end list -->
```py

class Engine:
    def start(self):
        print("Engine starting... Vroom!")

class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model
        # This car 'has an' Engine. This is composition.
        self.engine = Engine()

    def start_car(self):
        print(f"Starting the {self.make} {self.model}...")
        # The Car object tells its Engine object to start.
        self.engine.start()

# Create a car, which automatically creates an engine inside it.
my_car = Car("Ford", "Mustang")
my_car.start_car()
```
### Slide 3: Objects Passed as Arguments

  * Objects can also interact by being passed as arguments to each other's methods.
  * This allows for more flexible and decoupled interactions. For example, a `Mechanic` object could fix any `Car` object passed to it.

<!-- end list -->
```py

class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model
        self.is_broken = True

    def get_name(self):
        return f"{self.make} {self.model}"

class Mechanic:
    def fix_car(self, car_to_fix): # Takes a Car object as an argument
        if car_to_fix.is_broken:
            print(f"The mechanic is fixing the {car_to_fix.get_name()}.")
            car_to_fix.is_broken = False
            print(f"The {car_to_fix.get_name()} is now fixed!")
        else:
            print(f"The {car_to_fix.get_name()} is not broken.")

# Create our objects
my_car = Car("Honda", "Civic")
bob = Mechanic()

# The mechanic interacts with the car
bob.fix_car(my_car)
```
### Slide 4: Modeling Real-World Systems

  * Object interaction is key to modeling complex systems.
  * Consider a simple e-commerce system:
      * A `Customer` object might have a `ShoppingCart` object.
      * The `ShoppingCart` object would contain a list of `Product` objects.
      * When the `Customer` decides to checkout, the `ShoppingCart` might interact with a `PaymentProcessor` object.
  * Each object has its own responsibilities, and they work together to achieve a larger goal.

### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 16: "Classes and functions" and Chapter 18: "Inheritance" (which builds on these concepts).
  * **Practice Exercise:**
      * Create a `Student` class and a `Course` class.
      * Modify the `Student` class so that a student can enroll in a course. This might involve adding a `Course` object to a list of courses within the `Student` object.
      * Create a `Course` method `add_student(student)` that adds a student to an enrollment list for that course.
      * Create a few students and courses and have them interact.