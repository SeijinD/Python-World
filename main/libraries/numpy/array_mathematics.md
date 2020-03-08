[Back](../numpy.md)

# Array Mathimatics
---

- ##### Arithmetic Operations
  - ##### Subtraction
    ~~~~
    g = a - b
    ~~~~
  - ##### Subtraction
    ~~~~
    np.subtract(a,b)
    ~~~~
  - ##### Addition
    ~~~~
    g = a + b
    ~~~~
  - ##### Addition
    ~~~~
    np.add(a,b)
    ~~~~
  - ##### Division
    ~~~~
    g = a / b
    ~~~~
  - ##### Division
    ~~~~
    np.divide(a,b)
    ~~~~
  - ##### Multiplication
    ~~~~
    g = a * b
    ~~~~
  - ##### Multiplication
    ~~~~
    np.multiply(a,b)
    ~~~~
  - ##### Exponentiation
    ~~~~
    np.exp(b)
    ~~~~
  - ##### Square root
    ~~~~
    np.sqrt(b)
    ~~~~
  - ##### Print sines of an array
    ~~~~
    np.sin(a)
    ~~~~
  - ##### Element-wise cosine
    ~~~~
    np.cos(b)
    ~~~~
  - ##### Element-wise natural logarithm
    ~~~~
    np.log(a)
    ~~~~
  - ##### Dot product
    ~~~~
    e.dot(f)
    ~~~~
- ##### Comparison
  - ##### Element-wise comparison
    ~~~~
    a == b
    ~~~~
  - ##### Element-wise comparison
    ~~~~
    a < 2
    ~~~~
  - ##### Array-wise comparison
    ~~~~
    np.array_equal(a, b)
    ~~~~
- ##### Aggregate Functions
  - ##### Array-wise sum
    ~~~~
    a.sum()
    ~~~~
  - ##### Array-wise minimum value
    ~~~~
    a.min()
    ~~~~
  - ##### Maximum value of an array row
    ~~~~
    a.max(axis=0)
    ~~~~
  - ##### Cumulative sum of the elements
    ~~~~
    a.cumsum(axis=1)
    ~~~~
  - ##### Mean
    ~~~~
    a.mean()
    ~~~~
  - ##### Median
    ~~~~
    a.median()
    ~~~~
  - ##### Correlation coefficient
    ~~~~
    a.corrcoef()
    ~~~~
  - ##### Standard deviation
    ~~~~
    np.std(a)
    ~~~~
- ##### Copying Arrays
  - ##### Create a view of the array with the same data
    ~~~~
    h = a.view()
    ~~~~
  - ##### Create a copy of the array
    ~~~~
    np.copy(a)
    ~~~~
  - ##### Create a deep copy of the array
    ~~~~
    h = a.copy()
    ~~~~
- ##### Sorting Arrays
  - ##### Sort an array
    ~~~~
    a.sort()
    ~~~~
  - ##### Sort the elements of an array's axis
    ~~~~
    a.sort(axis=0)
    ~~~~