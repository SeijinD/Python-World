[Back](../numpy.md)

# I/O
---

- ##### Saving & Loading On Disk
```python
np.save('my_array', a)
np.savez('array.npz', a, b)
np.load('my_array.npy')
```
- ##### Saving & Loading Text Files
```python
np.loadtxt("myfile.txt")
np.genfromtxt("my_file.csv", delimiter=',')
np.savetxt("myarray.txt", a, delimiter=" ")
```