up:: [[Numerical Methods MOC]]
tags:: #Math 
# Sparse Matrices
- Sparse matrices are matrices that contain a large number of zero elements. 
- In numerical methods, especially when solving multidimensional [[PDE]] like the [[Two Dimensional Heat Equation]], sparse matrices are essential because they **improve efficiency in terms of memory and computational time**.
- [[Time Discretization]] in [[Finite Difference Methods]] will lead to a massive system of linear equations that needs to be solved at each time step:
$$Ax=b$$
where:
- A is the coefficient matrix representing the finite difference approximation (often sparse).
- x is the solution vector (e.g., temperature at each grid point).
- b is a vector of known values (boundary conditions, external heat sources, etc.).