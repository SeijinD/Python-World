[Back](../numpy.md)

# Array Manipulation
---

- #### Transposing Array
  - ##### Permute array dimensions
    ```python
    i = np.transpose(b)
    ```
- #### Changing Array Shape
  - ##### Flatten the array
    ```python
    b.ravel()
    ```
  - ##### Reshape, but don’t change data
    ```python
    g.reshape(3,-2)
    ```
- #### Adding/Removing Elements
  - ##### Return a new array with shape (2,6)
    ```python
    h.resize((2,6))
    ```
  - ##### Append items to an array
    ```python
    np.append(h,g)
    ```
  - ##### Insert items in an array
    ```python
    np.insert(a, 1, 5)
    ```
  - ##### Delete items from an array
    ```python
    np.delete(a,[1])
    ```
- #### Combining Arrays
  - ##### Concatenate arrays
    ```python
    np.concatenate((a,d),axis=0
    ```
  - ##### Stack arrays vertically (row-wise)
    ```python
    np.vstack((a,b))
    ```
  - ##### Stack arrays vertically (row-wise)
    ```python
    np.r_[e,f]
    ```
  - ##### Stack arrays horizontally (column-wise)
    ```python
    np.hstack((e,f))
    ```
  - ##### Create stacked column-wise arrays
    ```python
    np.column_stack((a,d))
    ```
  - ##### Create stacked column-wise arrays
    ```python
    np.c_[a,d]
    ```
- #### Splitting Arrays
  - ##### Split the array horizontally at the 3rd index
    ```python
    np.hsplit(a,3)
    ```
  - ##### Split the array vertically at the 2nd index
    ```python
    np.vsplit(c,2)
    ```