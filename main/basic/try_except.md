[Back](/main/basic.md)

# Try Except
---

- The **try** block lets you test a block of code for errors.
- The **except** block lets you handle the error.
- The **finally** block lets you execute code, regardless of the result of the try- and except blocks.

#### Example:
~~~~
try:
  print(x)
except:
  print("Something went wrong")
finally:
  print("The 'try except' is finished")
~~~~
~~~~
try:
  print(x)
except NameError:
  print("Variable x is not defined")
except:
  print("Something else went wrong") 
~~~~

- You can use the **else** keyword to define a block of code to be executed if no errors were raised.
~~~~
try:
  print("Hello")
except:
  print("Something went wrong")
else:
  print("Nothing went wrong") 
~~~~