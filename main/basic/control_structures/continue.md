[Back](/main/basic/control_structures.md)

# Continue
---

The continue statement is used to skip the rest of the code inside a loop for the current iteration only. Loop does not terminate but continues on with the next iteration.

#### Example:
~~~~
for val in "string":
    if val == "r":
        continue
    print(val)

print("The end.")
~~~~
#### Result:
~~~~
s
t
i
n
g
The end.
~~~~