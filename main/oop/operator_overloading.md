# Operator Overloading
---

You can change the meaning of an operator in Python depending upon the operands used. This practice is known as operating overloading.

Python operators work for built-in classes. But same operator behaves differently with different types. For example, the + operator will, perform arithmetic addition on two numbers, merge two lists and concatenate two strings.

This feature in Python, that allows same operator to have different meaning according to the context is called operator overloading.

#### Example:
```python
class Point:
    def __init__(self, x = 0, y = 0):
        self.x = x
        self.y = y
```
```python
# + operator for different purposes. 

print(1 + 2) # 3

# Concatenate two strings 
print("Geeks"+"For") # GeeksFor
  
# Product two numbers 
print(3 * 4) # 12
  
# Repeat the String 
print("Geeks"*4) # GeeksGeeksGeeksGeeks
```

#### Python magic methods or special functions for operator overloading

##### Binary Operators:
- \+
  - \_\_add\_\_(self, other)
- \-
  - \_\_sub\_\_(self, other)
- \*
  - \_\_mul\_\_(self, other)
- /
  - \_\_truediv\_\_(self, other)
- //
  - \_\_floordiv\_\_(self, other)
- %
  - \_\_mod\_\_(self, other)
- **
  - \_\_apow\_\_(self, other)
##### Comparison Operators :
- < 
  - \_\_lt\_\_(self, other)
- >
  - \_\_gt\_\_(self, other)
- <=
  - \_\_le\_\_(self, other)
- \>=
  - \_\_ge\_\_(self, other)
- ==
  - \_\_eq\_\_(self, other)
- !=
  - \_\_ne\_\_(self, other)
##### Assignment Operators :
- -=
  - \_\_isub\_\_(self, other)
- +=
  - \_\_iadd\_\_(self, other)
- *=
  - \_\_imul\_\_(self, other)
- /=
  - \_\_idiv\_\_(self, other)
- //=
  - \_\_ifloordiv\_\_(self, other)
- %=
  - \_\_imod\_\_(self, other)
- **=
  - \_\_ipow\_\_(self, other)