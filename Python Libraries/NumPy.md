```python
import numpy as np
```
# Linear Space vs Array Range
|        | np.arange()         | np.linspace()    |
| ------ | ------------------- | ---------------- |
| Range  | $(start,stop)$      | $(start,stop]$   |
| Points | Step between values | Number of values |

Both returns np.ndarray.
```python
array_range = np.arange(start, stop, step)
linear_space = np.linspace(start, stop, num)
```

## Example
Getting points between $0$ and 10 $(0, 10]$
```python
array_range = np.arange(0, 11, 2.5)
linear_space = np.linspace(0, 10, 5)
```
Both returns `[ 0. 2.5 5. 7.5 10. ]`

# Meshgrid
Creates 2d nparray out of 2 1d nparrays

```python
x = np.array([1, 2, 3, 4])
y = np.array([10, 20])
X, Y = np.meshgrid(x, y)

print(f'X: {X.shape}\n {X}')
print(f'Y: {Y.shape}\n {Y}')
#X: (2, 4)
# [[1 2 3 4]
# [1 2 3 4]]
#Y: (2, 4)
# [[10 10 10 10]
# [20 20 20 20]]
```
# Sources
https://numpy.org/doc/stable/reference/index.html

#DataScience
#ProgrammingLanguages/Python/Libraries