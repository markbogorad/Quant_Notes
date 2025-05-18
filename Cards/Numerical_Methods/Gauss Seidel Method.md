up:: [[Numerical Methods MOC]]
tags:: #Math 
# Gauss Seidel Method
$$x_i^{(k+1)} = \frac{1}{A_{ii}} \left( b_i - \sum_{j < i} A_{ij} x_j^{(k+1)} - \sum_{j > i} A_{ij} x_j^{(k)} \right)$$
- Similar to Jacobi but uses the latest available values as soon as they are computed.
- Usually converges faster than the Jacobi method.
