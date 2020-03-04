# For Loops
---

The for loop in Python is used to iterate over a sequence (list, tuple, string) or other iterable objects. 

#### For:
~~~~
for val in sequence:
	Body of for
~~~~

#### For with Else:
~~~~
for val in sequence:
	Body of for
else:
    Body of else
~~~~

#### Range:

- We can generate a sequence of numbers using range() function. range(10) will generate numbers from 0 to 9 (10 numbers).
~~~~
for i in range(10):
    Body of for
~~~~
- We can also define the start, stop and step size as range(start,stop,step size). step size defaults to 1 if not provided.
~~~~
for i in range(10,2):
    Body of for
~~~~
- This function does not store all the values in memory, it would be inefficient. So it remembers the start, stop, step size and generates the next number on the go.
~~~~
for i in range(2,30,3):
    Body of for
~~~~
- To force this function to output all the items, we can use the function list().
~~~~
print(list(range(10)))
~~~~