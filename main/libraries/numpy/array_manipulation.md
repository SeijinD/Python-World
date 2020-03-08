[Back](../numpy.md)

# Array Manipulation
---

- #### Transposing Array
  - ##### Permute array dimensions
    ~~~~
    i = np.transpose(b)
    ~~~~
- #### Changing Array Shape
  - ##### Flatten the array
    ~~~~
    b.ravel()
    ~~~~
  - ##### Reshape, but don’t change data
    ~~~~
    g.reshape(3,-2)
    ~~~~
- #### Adding/Removing Elements
  - ##### Return a new array with shape (2,6)
    ~~~~
    h.resize((2,6))
    ~~~~
  - ##### Append items to an array
    ~~~~
    np.append(h,g)
    ~~~~
  - ##### Insert items in an array
    ~~~~
    np.insert(a, 1, 5)
    ~~~~
  - ##### Delete items from an array
    ~~~~
    np.delete(a,[1])
    ~~~~
- #### Combining Arrays
  - ##### Concatenate arrays
    ~~~~
    np.concatenate((a,d),axis=0
    ~~~~
  - ##### Stack arrays vertically (row-wise)
    ~~~~
    np.vstack((a,b))
    ~~~~
  - ##### Stack arrays vertically (row-wise)
    ~~~~
    np.r_[e,f]
    ~~~~
  - ##### Stack arrays horizontally (column-wise)
    ~~~~
    np.hstack((e,f))
    ~~~~
  - ##### Create stacked column-wise arrays
    ~~~~
    np.column_stack((a,d))
    ~~~~
  - ##### Create stacked column-wise arrays
    ~~~~
    np.c_[a,d]
    ~~~~
- #### Splitting Arrays
  - ##### Split the array horizontally at the 3rd index
    ~~~~
    np.hsplit(a,3)
    ~~~~
  - ##### Split the array vertically at the 2nd index
    ~~~~
    np.vsplit(c,2)
    ~~~~