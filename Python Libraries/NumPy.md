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

# Sources
https://numpy.org/doc/stable/reference/index.html

#DataScience
#ProgrammingLanguages/Python/Libraries