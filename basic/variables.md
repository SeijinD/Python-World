# Variables
---

- Variables are containers for storing data values.
- Unlike other programming languages, Python has no command for declaring a variable.
- A variable is created the moment you first assign a value to it.

#### Example:
~~~~
z = 5
y = "John"
~~~~
~~~~
x = 4 # x is of type int
x = "Sally" # x is now of type str
~~~~

#### Variable Names
- A variable can have a short name (like x and y) or a more descriptive name (age, carname, total_volume). Rules for Python variables:
- A variable name must start with a letter or the underscore character
- A variable name cannot start with a number
- A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ )
- Variable names are case-sensitive (age, Age and AGE are three different variables)

#### Assign Value to Multiple Variables
~~~~
x, y, z = "Orange", "Banana", "Cherry"
~~~~
#### Same value to multiple variables in one line:
~~~~
x, y, z = "Orange"
~~~~
#### To combine both text and a variable, Python uses the + character:
~~~~
x = "awesome"
print("Python is " + x)
~~~~
~~~~
x = "Python is "
y = "awesome"
z =  x + y
~~~~