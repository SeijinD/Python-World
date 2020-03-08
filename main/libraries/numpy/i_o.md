[Back](../numpy.md)

# I/O
---

- ##### Saving & Loading On Disk
~~~~
np.save('my_array', a)
np.savez('array.npz', a, b)
np.load('my_array.npy')
~~~~
- ##### Saving & Loading Text Files
~~~~
np.loadtxt("myfile.txt")
np.genfromtxt("my_file.csv", delimiter=',')
np.savetxt("myarray.txt", a, delimiter=" ")
~~~~