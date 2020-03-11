[Back](../numpy.md)

# Initial Placeholders
---

- ##### Create an array of zeros
```python
np.zeros((3,4))
```
- ##### Create an array of ones
```python
np.ones((2,3,4),dtype=np.int16)
```
- ##### Create an array of evenly spaced values (step value)
```python
d = np.arange(10,25,5)
```
- ##### Create an array of evenly spaced values (number of samples)
```python
np.linspace(0,2,9)
```
- ##### Create a constant array
```python
e = np.full((2,2),7)
```
- ##### Create a 2X2 identity matrix
```python
f = np.eye(2)
```
- ##### Create an array with random values
```python
np.random.random((2,2))
```
- ##### Create an empty array
```python
np.empty((3,2))
```
