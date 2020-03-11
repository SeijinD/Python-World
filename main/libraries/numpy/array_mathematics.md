[Back](../numpy.md)

# Array Mathimatics
---

- ##### Arithmetic Operations
  - ##### Subtraction
    ```python
    g = a - b
    ```
  - ##### Subtraction
    ```python
    np.subtract(a,b)
    ```
  - ##### Addition
    ```python
    g = a + b
    ```
  - ##### Addition
    ```python
    np.add(a,b)
    ```
  - ##### Division
    ```python
    g = a / b
    ```
  - ##### Division
    ```python
    np.divide(a,b)
    ```
  - ##### Multiplication
    ```python
    g = a * b
    ```
  - ##### Multiplication
    ```python
    np.multiply(a,b)
    ```
  - ##### Exponentiation
    ```python
    np.exp(b)
    ```
  - ##### Square root
    ```python
    np.sqrt(b)
    ```
  - ##### Print sines of an array
    ```python
    np.sin(a)
    ```
  - ##### Element-wise cosine
    ```python
    np.cos(b)
    ```
  - ##### Element-wise natural logarithm
    ```python
    np.log(a)
    ```
  - ##### Dot product
    ```python
    e.dot(f)
    ```
- ##### Comparison
  - ##### Element-wise comparison
    ```python
    a == b
    ```
  - ##### Element-wise comparison
    ```python
    a < 2
    ```
  - ##### Array-wise comparison
    ```python
    np.array_equal(a, b)
    ```
- ##### Aggregate Functions
  - ##### Array-wise sum
    ```python
    a.sum()
    ```
  - ##### Array-wise minimum value
    ```python
    a.min()
    ```
  - ##### Maximum value of an array row
    ```python
    a.max(axis=0)
    ```
  - ##### Cumulative sum of the elements
    ```python
    a.cumsum(axis=1)
    ```
  - ##### Mean
    ```python
    a.mean()
    ```
  - ##### Median
    ```python
    a.median()
    ```
  - ##### Correlation coefficient
    ```python
    a.corrcoef()
    ```
  - ##### Standard deviation
    ```python
    np.std(a)
    ```
- ##### Copying Arrays
  - ##### Create a view of the array with the same data
    ```python
    h = a.view()
    ```
  - ##### Create a copy of the array
    ```python
    np.copy(a)
    ```
  - ##### Create a deep copy of the array
    ```python
    h = a.copy()
    ```
- ##### Sorting Arrays
  - ##### Sort an array
    ```python
    a.sort()
    ```
  - ##### Sort the elements of an array's axis
    ```python
    a.sort(axis=0)
    ```