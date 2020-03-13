[Back](/main/oop.md)

# Encapsulation
---

Using OOP in Python, we can restrict access to methods and variables. This prevent data from direct modification which is called encapsulation. In Python, we denote private attribute using underscore as prefix i.e single “ _ “ or double “ __“.

#### Example:
```python
class Computer:

    def __init__(self):
        self.__maxprice = 900

    def sell(self):
        print("Selling Price: {}".format(self.__maxprice))

    def setMaxPrice(self, price):
        self.__maxprice = price

c = Computer()
c.sell() # Selling Price: 900

# Change the price
c.__maxprice = 1000
c.sell() # Selling Price: 900

# Using setter function
c.setMaxPrice(1000)
c.sell() # Selling Price: 1000
```