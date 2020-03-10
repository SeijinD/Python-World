[Back](../libraries.md)

# NumPy
---

#### What is NumPy?
Numpy is the core library for scientific computing in Python. It provides a high-performance multidimensional array object, and tools for working with these arrays. 

NumPy is often used along with packages like [SciPy](scipy.md) (Scientific Python) and [Matplotlib](matplotlib.md)  (plotting library). This combination is widely used as a replacement for MatLab, a popular platform for technical computing. However, Python alternative to MatLab is now seen as a more modern and complete programming language.

#### Install NumPy
~~~~
pip install numpy
~~~~

#### Import NumPy
~~~~
import numpy as np
~~~~

#### Create Arrays
~~~~
a = np.array([1,2,3])
b = np.array([(1.5,2,3), (4,5,6)], dtype = float)
c = np.array([[(1.5,2,3), (4,5,6)], [(3,2,1), (4,5,6)]], dtype = float)
d = np.array( [ [1,2], [3,4] ], dtype=complex )
~~~~

#### Print Arrays
~~~~
>>> a = np.arange(6)                         # 1d array
>>> print(a)
[0 1 2 3 4 5]
>>>
>>> b = np.arange(12).reshape(4,3)           # 2d array
>>> print(b)
[[ 0  1  2]
 [ 3  4  5]
 [ 6  7  8]
 [ 9 10 11]]
>>>
>>> c = np.arange(24).reshape(2,3,4)         # 3d array
>>> print(c)
[[[ 0  1  2  3]
  [ 4  5  6  7]
  [ 8  9 10 11]]
 [[12 13 14 15]
  [16 17 18 19]
  [20 21 22 23]]]
~~~~

- #### [Data Types](numpy/data_types.md)

- #### [Initial Placeholders](numpy/initial_placeholders.md)

- #### [Inspecting Your Array](numpy/inspecting_your_array.md)

- #### [Array Mathematics](numpy/array_mathematics.md)

- #### [Subsetting-Slicing-Indexing](numpy/subsetiing_slicing_indexing.md)

- #### [Array Manipulation](numpy/array_manipulation.md)

- #### [I/O](numpy/i_o.md)