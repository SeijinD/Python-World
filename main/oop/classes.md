[Back](/main/oop.md)

# Classes
---

A class is a blueprint for the object.

#### Example:
```python
class Dog:
    pass
```

We create a new **class** using the class statement and the name of the class. This is followed by an indented block of statements which form the body of the class. In this case, we have an empty block which is indicated using the **pass** statement.

#### Example:
```python
class Dog:
    # Class attribute
    species = 'mammal'

    # Initializer / Instance attributes
    # __init__ is name for Constructor/Initializer
    def __init__(self, name, age):
        self.name = name
        self.age = age

    # instance method
    def description(self):
        return "{} is {} years old".format(self.name, self.age)

    # instance method
    def speak(self, sound):
        return "{} says {}".format(self.name, sound)

```
Print object (toString):
```python
# __str__ is a good practice to use for name.
def __str__(self):
        return self.firstName + " " + self.lastName
```