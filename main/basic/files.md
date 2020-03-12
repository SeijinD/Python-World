[Back](/main/basic.md)

# Files
---

- #### What is a file?

File is a named location on disk to store related information. It is used to permanently store data in a non-volatile memory (e.g. hard disk).
File handling is an important part of any web application and generally.
Python has several functions for creating, reading, updating, and deleting files.

- #### File Handling

The key function for working with files in Python is the **open()** function.
The **open()** function takes two parameters; **filename**, and **mode**.

There are four different methods (modes) for opening a file:
- **"r"** 
  - Read - Default value. Opens a file for reading, error if the file does not exist
- **"a"** 
  - Append - Opens a file for appending, creates the file if it does not exist
- **"w"** 
  - Write - Opens a file for writing, creates the file if it does not exist
- **"x"** 
  - Create - Creates the specified file, returns an error if the file exists

In addition you can specify if the file should be handled as **binary** or **text** mode:
- **"t"**
    - Text - Default value. Text mode
- **"b"**
  - Binary - Binary mode (e.g. images)
  
- #### Examples:
```python
f = open("demofile.txt")
f = open("demofile2.txt", "r")
f = open("demofile3.txt",mode = 'r',encoding = 'utf-8') # Add encdoding mode.

#Two different ways
f = open("test.txt")    # Open file in current directory
f = open("C:/Python33/README.txt")  # Specifying full path (Bad way)
```

Closing a file will free up the resources that were tied with the file and is done using Python close() method.

Python has a garbage collector to clean up unreferenced objects but, we must not rely on it to close the file.
```python
f = open("test.txt",encoding = 'utf-8')
# perform file operations
f.close()
```

- #### Read File
The open() function returns a file object, which has a read() method for reading the content of the file:
```python
f = open("demofile.txt", "r")
print(f.read()) 

f = open("demofile.txt", "r")
print(f.read(5)) # Return the 5 first characters of the file.

f = open("demofile.txt", "r")
print(f.readline()) # Read one line of the file.
```

- #### Write File
To write to an existing file, you must add a parameter to the open() function:

- **"a"** 
  - Append - will append to the end of the file
- **"w"** 
  - Write - will overwrite any existing content

```python
f = open("demofile2.txt", "a")
f.write("Now the file has more content!")
f.close()

f = open("demofile3.txt", "w") # The "w" method will overwrite the entire file.
f.write("Woops! I have deleted the content!")
f.close()
```

- #### Create a New File
  
To create a new file in Python, use the open() method, with one of the following parameters:

- **"x"** 
  - Create - will create a file, returns an error if the file exist
- **"a"** 
  - Append - will create a file if the specified file does not exist
- **"w"** 
  - Write - will create a file if the specified file does not exist

```python
f = open("myfile.txt", "x") # Create a file called "myfile.txt"
f = open("myfile.txt", "a") # Create a new file if it does not exist
f = open("myfile.txt", "w") # Create a new file if it does not exist
```

- #### Delete

##### Delete a File
To delete a file, you must import the OS module, and run its **os.remove()** function:

```python
import os
os.remove("demofile.txt") 
```
##### Check if File exist
To avoid getting an error, you might want to check if the file exists before you try to delete it:

```python
import os
if os.path.exists("demofile.txt"):
  os.remove("demofile.txt")
else:
  print("The file does not exist") 
```
##### Delete a Folder
To delete an entire folder, use the **os.rmdir()** method:
```python
import os
os.rmdir("myfolder") 
```

- #### With Statement*

With the **"With"** statement, you get better syntax and exceptions handling. 
In addition, it will **automatically close** the file. The with statement provides a way for ensuring that a clean-up is always used.

```python
with open('output.txt', 'w') as file:
    file.write('Hi there!')

with open("welcome.txt") as file:
   data = file.read()
```