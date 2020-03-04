# Pass
---

Pass is a null statement. The difference between a comment and pass statement in Python is that, while the interpreter ignores a comment entirely, pass is not ignored.
However, nothing happens when pass is executed. It results into no operation (NOP).

#### Example:
~~~~
for val in "string":
    if val == "r":
        pass
    print(val)

print("The end.")
~~~~
#### Result:
~~~~
s
t
r
i
n
g
The end.
~~~~

#### We can do the same thing in an empty function or class as well:
~~~~
def function(args):
    pass
~~~~
~~~~
class example:
    pass
~~~~