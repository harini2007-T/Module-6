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
