up:: [[Python MOC]]
tags:: #Programming 
# Vectorization
- Operations are applied to entire arrays or sequences of data at once rather than iterating through individual elements one by one
- Vectorized operations are also more memory efficient, as they often avoid the overhead associated with explicit loops in high-level languages like Python.

## Simple Example
```
a = np.array([1, 2, 3])
b = 2  # Scalar

# Vectorized multiplication with broadcasting
c = a * b
print(c)  # Outputs: [2, 4, 6]

```