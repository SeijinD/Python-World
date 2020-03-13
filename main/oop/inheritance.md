[Back](/main/oop.md)

# Inheritance
---

Instead of starting from scratch, you can create a class by deriving it from a preexisting class by listing the parent class in parentheses after the new class name.
The child class inherits the attributes of its parent class, and you can use those attributes as if they were defined in the child class. A child class can also override data members and methods from the parent.

#### Example:
```python
# Parent class
class Bird:
    
    def __init__(self):
        print("Bird is ready")

    def whoisThis(self):
        print("Bird")

    def swim(self):
        print("Swim faster")

# Child class
class Penguin(Bird):

    def __init__(self):
        # Call super() function
        super().__init__()
        print("Penguin is ready")

    def whoisThis(self):
        print("Penguin")

    def run(self):
        print("Run faster")

peggy = Penguin()
# Bird is ready
# Penguin is ready

peggy.whoisThis() # Penguin
peggy.swim() # Swim faster
peggy.run() # Run faster
```

## Multiple Inheritance

In multiple inheritance, the features of all the base classes are inherited into the derived class. The syntax for multiple inheritance is similar to single inheritance.

#### Example:
```python
class Base1:
    pass

class Base2:
    pass

class MultiDerived(Base1, Base2):
    pass
```

## Multilevel  Inheritance

In multilevel inheritance, features of the base class and the derived class is inherited into the new derived class.

#### Example:
```python
class Base:
    pass

class Derived1(Base):
    pass

class Derived2(Derived1):
    pass
```