# NumPy Tips
---

- #### Change in numpy array, min and max in all values in array with operation:
~~~~
a = np.array([1.2, 1.0, 0.0, 0.2, -0.2, 0.5, -0.5])

a[a > 1.0] = 1.0 # max
=> a == array([1.0, 1.0, 0.0, 0.2, -0.2, 0.5, -0.5])

a[a < 0.0] = 0.0 # min
=> a == array([1.0, 1.0, 0.0, 0.2, 0.0, 0.5, 0.0])
~~~~

