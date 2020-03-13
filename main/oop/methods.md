[Back](/main/oop.md)

# Methods
---

Methods are functions defined inside the body of a class. They are used to define the behaviors of an object.

#### Example:
```python
# With parameters
def speak(self, sound):
        return "{} says {}".format(self.name, sound)
```
```python
# Without parameters
def description(self):
        return "{} is {} years old".format(self.name, self.age)
```
```python
# Call method without parameters
print(mikey.description()) 
# Call method with parameters
print(mikey.speak("Gruff Gruff")) 
```