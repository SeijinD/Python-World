# Break
---

The break statement terminates the loop containing it. Control of the program flows to the statement immediately after the body of the loop.
If break statement is inside a nested loop (loop inside another loop), break will terminate the innermost loop.

#### Example:
~~~~
for val in "string":
    if val == "r":
        break
    print(val)

print("The end.")
~~~~
#### Result:
~~~~
s
t
The end.
~~~~