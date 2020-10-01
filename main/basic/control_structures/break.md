[Back](/main/basic/control_structures.md)

# Break
---

The break statement terminates the loop containing it. Control of the program flows to the statement immediately after the body of the loop.
If break statement is inside a nested loop (loop inside another loop), break will terminate the innermost loop.The most common use for break is when some external condition is triggered requiring a hasty exit from a loop. The break statement can be used in both while and for loops.

#### Example:
```python
for val in "string":
    if val == "r":
        break
    print(val)

print("The end.")
```
#### Result:
~~~~
s
t
The end.
~~~~


#### Example:
```python
var = 10                   
while var > 0:              
   print 'Current variable value :', var
   var = var -1
   if var == 5:
      break

print "Good bye!"
```
#### Result:
~~~~
Current variable value : 10
Current variable value : 9
Current variable value : 8
Current variable value : 7
Current variable value : 6
Good bye!
~~~~
