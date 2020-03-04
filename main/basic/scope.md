# Scope
---

A variable is only available from inside the region it is created. This is called scope.

### Local Scope
A variable created inside a function belongs to the local scope of that function, and can only be used inside that function.

#### Example
~~~~
def myfunc():
  x = 300
  print(x)

myfunc() 

Output: 300
~~~~

### Global Scope
A variable created in the main body of the Python code is a global variable and belongs to the global scope.
Global variables are available from within any scope, global and local.

#### Example
~~~~
x = 300

def myfunc():
  print(x)

myfunc()

print(x)

Output: 300
        300
~~~~

### Global Keyword
If you need to create a global variable, but are stuck in the local scope, you can use the **global** keyword.
The **global** keyword makes the variable global.

#### Example
~~~~
def myfunc():
  global x
  x = 300

myfunc()

print(x)

Output: 300
~~~~