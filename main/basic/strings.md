[Back](/main/basic.md)

# Strings
---

String literals in python are surrounded by either single quotation marks, or double quotation marks.

**'hello'** is the same as **"hello"**.


#### Assign String to a Variable
```python
a = "Hello"
```

#### Multiline Strings
```python
a = """Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua."""
```

###### or
```python
a = '''Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua.'''
```

###### Strings are Arrays
Like many other popular programming languages, strings in Python are arrays of bytes representing unicode characters.
```python
a = "Hello, World!"
print(a[1])
Output: e
```

###### Slicing
You can return a range of characters by using the slice syntax.
```python
b = "Hello, World!"
print(b[2:5])
Output: llo
```

###### Negative Indexing
Use negative indexes to start the slice from the end of the string.
```python
b = "Hello, World!"
print(b[-5:-2])
Output: orl
```

###### String Length
To get the length of a string, use the **len()** function.
```python
a = "Hello, World!"
print(len(a))
Output: 13
```

###### Other Methods

The **strip()** method removes any whitespace from the beginning or the end:
```python
a = " Hello, World! "
print(a.strip())
Output: "Hello, World!"
```

The **lower()** method returns the string in lower case:
```python
a = "Hello, World!"
print(a.lower())
```

The **upper()** method returns the string in upper case:
```python
a = "Hello, World!"
print(a.upper()) 
```

The **swapcase()** method returns the string with swap upper and lower case:
```python
a = "Hello, World!"
print(a.upper()) 
```

The **replace()** method replaces a string with another string:
```python
a = "Hello, World!"
print(a.replace("H", "J"))
```

The **split()** method splits the string into substrings if it finds instances of the separator:
```python
a = "Hello, World!"
print(a.split(","))
Output: ['Hello', ' World!'] 
```

Check if the phrase "ain" is present in the following text:
```python
txt = "The rain in Spain stays mainly in the plain"
x = "ain" in txt
print(x)
Output: True
```

Check if the phrase "ain" is NOT present in the following text:
```python
txt = "The rain in Spain stays mainly in the plain"
x = "ain" not in txt
print(x) 
Output: False
```

To concatenate, or combine, two strings you can use the + operator.
```python
a = "Hello"
b = "World"
c = a + b
print(c)
Output: HelloWorld
```

To add a space between them, add a " ":
```python
a = "Hello"
b = "World"
c = a + " " + b
print(c)
Output: Hello World
```
