[Back](/main/basic.md)

# Booleans
---

Booleans represent one of two values: True or False.

The bool() function allows you to evaluate any value, and give you True or False in return:
~~~~
print(bool("Hello"))
print(bool(15))
~~~~
~~~~
x = "Hello"
y = 15

print(bool(x))
print(bool(y))
~~~~

#### Most Values are True
- Almost any value is evaluated to True if it has some sort of content.
- Any string is True, except empty strings.
- Any number is True, except 0.
- Any list, tuple, set, and dictionary are True, except empty ones.

#### Some Values are False
- In fact, there are not many values that evaluates to False, except empty values, such as (), [], {}, "", the number 0, and the value None.
- And of course the value False evaluates to False.