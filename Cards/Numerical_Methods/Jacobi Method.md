up:: [[Numerical Methods MOC]]
tags:: #Math 
# Jacobi Method
$$x_i^{(k+1)} = \frac{1}{A_{ii}} \left( b_i - \sum_{j \neq i} A_{ij} x_j^{(k)} \right)$$
- One of the simplest relaxation methods.
- Updates each component of xx independently using the previous iteration values.
- Convergence is guaranteed if AA is diagonally dominant.
