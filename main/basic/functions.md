[Back](/main/basic.md)

# Functions
---

- In Python, function is a group of related statements that perform a specific task.
- Functions help break our program into smaller and modular chunks. As our program grows larger and larger, functions make it more organized and manageable.
- Furthermore, it avoids repetition and makes code reusable.

### Syntax of Function
~~~~
def function_name(parameters):
	"""docstring"""
	statement(s)
~~~~

Above shown is a function definition which consists of following components.
- Keyword **def** marks the start of function header.
- A function name to uniquely identify it. Function naming follows the same rules of writing identifiers in Python.
- Parameters (arguments) through which we pass values to a function. They are optional.
- A colon **:** to mark the end of function header.
- Optional documentation string (docstring) to describe what the function does.
- One or more valid python statements that make up the function body. Statements must have same indentation level (usually 4 spaces).
- An optional return statement to return a value from the function.

### Calling a Function
~~~~
def my_function():
  print("Hello from a function")

my_function()
~~~~

### Parameters or Arguments?
From a function's perspective:
- A parameter is the variable listed inside the parentheses in the function definition.
- An argument is the value that are sent to the function when it is called.

### Number of Arguments
By default, a function must be called with the correct number of arguments. Meaning that if your function expects 2 arguments, you have to call the function with 2 arguments, not more, and not less.
~~~~
def my_function(fname, lname):
  print(fname + " " + lname)

my_function("Emil", "Refsnes") 
~~~~

### Arbitrary Arguments, *args
If you do not know how many arguments that will be passed into your function, add a * before the parameter name in the function definition.
~~~~
def my_function(*kids):
  print("The youngest child is " + kids[2])

my_function("Emil", "Tobias", "Linus") 
~~~~

### Keyword Arguments
You can also send arguments with the key = value syntax.
This way the order of the arguments does not matter.
~~~~
def my_function(child3, child2, child1):
  print("The youngest child is " + child3)

my_function(child1 = "Emil", child2 = "Tobias", child3 = "Linus") 
~~~~

### Arbitrary Keyword Arguments, **kwargs
If you do not know how many keyword arguments that will be passed into your function, add two asterisk: ** before the parameter name in the function definition.
~~~~
def my_function(**kid):
  print("His last name is " + kid["lname"])

my_function(fname = "Tobias", lname = "Refsnes") 
~~~~

### Default Parameter Value
The following example shows how to use a default parameter value.
~~~~
def my_function(country = "Norway"):
  print("I am from " + country)

my_function("Sweden")
my_function("India")
my_function()
my_function("Brazil") 
~~~~

### Passing a List as an Argument
You can send any data types of argument to a function (string, number, list, dictionary etc.), and it will be treated as the same data type inside the function.
~~~~
def my_function(food):
  for x in food:
    print(x)

fruits = ["apple", "banana", "cherry"]

my_function(fruits)
~~~~

### Return Values
To let a function return a value, use the **return** statement:
~~~~
def my_function(x):
  return 5 * x

print(my_function(3))
print(my_function(5))
print(my_function(9)) 
~~~~

### The pass Statement
**Function** definitions cannot be empty, but if you for some reason have a **function** definition with no content, put in the **pass** statement to avoid getting an error.
~~~~
def myfunction():
  pass
~~~~