# 🐍 Python OOP: Abstract Class & Method Example

## 🎯 AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

---

## 🧠 ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

---

## 💻 Program
```
from abc import ABC, abstractmethod
import math
class Shape(ABC):

    @abstractmethod
    def calculate_area(self):
        pass
class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def calculate_area(self):
        return self.width * self.height
class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def calculate_area(self):
        return math.pi * (self.radius ** 2)
rect = Rectangle(5, 3)
print("Rectangle area:", rect.calculate_area())

circle = Circle(4)
print("Circle area:", circle.calculate_area())
```
## Output
<img width="325" height="59" alt="Screenshot 2025-10-15 102519" src="https://github.com/user-attachments/assets/1b9c0bac-b52a-47b9-b36f-1d85edec9cb8" />

## Result
The program successfully calculates area of shapes using abstarct method and classes

# 🐟 Method Overriding-Fish and Shark Class Inheritance in Python

## 🧠 AIM:
To write a Python program that demonstrates class inheritance by creating a parent class `Fish` with a method `type`, and a child class `Shark` that overrides the `type` method.

## 📋 ALGORITHM:

1. Define the `Fish` class with a method named `type()` that prints `"fish"`.
2. Define the `Shark` class as a subclass of `Fish`, and override the `type()` method to print `"shark"`.
3. Create an instance of the `Fish` class named `obj_goldfish`.
4. Create an instance of the `Shark` class named `obj_hammerhead`.
5. Use a `for` loop to iterate over both objects.
6. Within the loop, call the `type()` method using the loop variable.
7. Output will demonstrate method overriding: printing `"fish"` and `"shark"` accordingly.

## 💻 PROGRAM:
```
class Fish:
    def type(self):
        return "I am a fish."
class Shark(Fish):
    def type(self):
        return "I am a shark, a type of fish."
fish = Fish()
print(fish.type())  # Output: I am a fish.

shark = Shark()
print(shark.type())  # Output: I am a shark, a type
```
## OUTPUT
<img width="311" height="63" alt="Screenshot 2025-10-15 103016" src="https://github.com/user-attachments/assets/ad84fe28-8599-418f-8c0a-adc3eb252ddf" />

## RESULT
The program successfully creates class inheritance

# 🐍 Python OOP: Encapsulation with Private Members

## 🎯 AIM

To implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth`.

---

## 🧠 ALGORITHM

1. **Define the Class**:
   - Create a class `Rectangle` with two private attributes: `__length` and `__breadth`.

2. **Initialize Variables**:
   - Use the `__init__()` constructor to set initial values for `__length` and `__breadth`.

3. **Print Values**:
   - Display the private variables from within the class to demonstrate access.

4. **Instantiate the Object**:
   - Create an object of the `Rectangle` class to trigger the constructor.

---

## 💻 Program
```
# Encapsulation Example in Python

class Rectangle:
    # Constructor to initialize private variables
    def __init__(self, length, breadth):
        self.__length = length      # Private attribute
        self.__breadth = breadth    # Private attribute

    # Method to display private values
    def display(self):
        print("Length:", self.__length)
        print("Breadth:", self.__breadth)

# Create an object of the Rectangle class
rect = Rectangle(10, 5)

# Display private members using class method
rect.display()
```
## Output
<img width="310" height="84" alt="image" src="https://github.com/user-attachments/assets/df418e57-b375-4bdf-8f11-2e0def3c72ec" />


## Result
The program successfully demonstrates Encapsulation in Python by defining a class with private data members (__length and __breadth).
The private variables are accessed only through class methods, ensuring data protection and controlled access.

# # 🐍 Python OOP: Polymorphism with Classes

## 🎯 AIM

To create two specific classes — `Beans` and `Mango`. Then, create a **generic function** that can accept any object and determine its **type** (Fruit or Vegetable) and **color**, using polymorphism.

---

## 🧠 ALGORITHM

1. **Create Class `Beans`**:
   - Define `type()` method that prints `"Vegetable"`.
   - Define `color()` method that prints `"Green"`.

2. **Create Class `Mango`**:
   - Define `type()` method that prints `"Fruit"`.
   - Define `color()` method that prints `"Yellow"`.

3. **Define Generic Function `func(obj)`**:
   - Call `obj.type()` and `obj.color()` — this works with both `Beans` and `Mango` objects, showcasing **polymorphism**.

4. **Create Objects**:
   - Instantiate `Beans` and `Mango`.
   - Pass them to `func()` and execute the program.

---

## 💻 Program
```
from abc import ABC, abstractmethod
class Food(ABC):
    @abstractmethod
    def get_type(self) -> str:
        pass

    @abstractmethod
    def get_color(self) -> str:
        pass
class Beans(Food):
    def get_type(self) -> str:
```
## Output
<img width="469" height="64" alt="Screenshot 2025-10-15 111137" src="https://github.com/user-attachments/assets/ad53e56b-044f-4794-9b1b-f84c655f854c" />

## Result
The program successfully creates class and returns type  using polymorphism

# 🐍 Python OOP: Operator Overloading (Less Than `<`)

## 🎯 AIM

To write a Python program that demonstrates **operator overloading** by overloading the **less than (`<`)** operator using a custom class.

---

## 🧠 ALGORITHM

1. **Create Class `A`**:
   - Define the `__init__()` method to initialize the object with a value `a`.

2. **Overload the `<` Operator**:
   - Define the `__lt__()` method with logic:
     - If `self.a < o.a`, return `"ob1 is less than ob2"`
     - Else, return `"ob2 is less than ob1"`

3. **Create Objects**:
   - Instantiate two objects `ob1` and `ob2` with values.

4. **Use `<` Operator**:
   - Use `print(ob1 < ob2)` to trigger the overloaded behavior.

---

## 💻 Program
# Operator Overloading Example: Less Than (<)

class A:
    def __init__(self, a):
        self.a = a

    # Overloading the < operator
    def __lt__(self, o):
        if self.a < o.a:
            return "ob1 is less than ob2"
        else:
            return "ob2 is less than ob1"

# Create two objects
ob1 = A(10)
ob2 = A(20)

# Compare using < operator
print(ob1 < ob2)


## Output
<img width="277" height="90" alt="image" src="https://github.com/user-attachments/assets/177551bc-d580-48d7-972e-b612a4b99d88" />


## Result
The program successfully demonstrates operator overloading by redefining the less than (<) operator in a custom class.
When comparing two objects, the overloaded method __lt__() executes, producing a descriptive comparison result instead of a boolean value.
