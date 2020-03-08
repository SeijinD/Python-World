[Back](../numpy.md)

# Subsetting-Slicing-Indexing
---

- #### Subsetting
    - ##### Select the element at the 2nd index
    ~~~~
    a[2]
    ~~~~
    - ##### Select the element at row 0 column 2 (equivalent to b[1][2])
    ~~~~
    b[1,2]
    ~~~~
- #### Slicing
    - ##### Select items at index 0 and 1
    ~~~~
    a[0:2]
    ~~~~
    - ##### Select items at rows 0 and 1 in column 1
    ~~~~
    b[0:2,1]
    ~~~~
    - ##### Select all items at row 0 (equivalent to b[0:1, :])
    ~~~~
    b[:1]
    ~~~~
    ###### Same as [1,:,:]
    ~~~~
    c[1,...]
    ~~~~
    - ##### Reversed array a
    ~~~~
    a[ : :-1]
    ~~~~
- #### Boolean Indexing
    - ##### Select elements from a less than 2
    ~~~~
    a[a<2]
    ~~~~
- #### Fancy Indexing
  - ##### Select elements (1,0),(0,1),(1,2) and (0,0)
    ~~~~
    b[[1, 0, 1, 0],[0, 1, 2, 0]]
    ~~~~
  - ##### Select a subset of the matrix’s rows and columns
    ~~~~
    b[[1, 0, 1, 0]][:,[0,1,2,0]]
    ~~~~