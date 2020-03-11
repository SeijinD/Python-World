[Back](/main/basic.md)

# Lambda Functions
---

In Python, lambda expressions (or lambda forms) are used to construct anonymous functions. To do so, you will use the **lambda** keyword (just as you use **def** to define normal functions).

Every anonymous function you define in Python will have 3 essential parts:

- The lambda keyword.
- The parameters (or bound variables), and
- The function body.

#### Example of Lambda Function:

```python
double = lambda x: x * 2

# Output: 10
print(double(5))
```
In the above program, **lambda x: x * 2** is the **lambda function**. Here **x** is the **argument** and **x * 2** is the **expression** that gets evaluated and returned.