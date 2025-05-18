up:: [[Numerical Methods MOC]]
tags:: #Math 
# Relaxation Methods
- Direct methods like Gaussian elimination is not possible for [[Sparse Matrices]], so these methods are introduced
- Relaxation methods are iterative techniques that improve an initial guess at the solution by updating it step by step until it converges.
- Each update incorporates local information from neighboring grid points, mimicking the heat diffusion process:
	- [[Jacobi Method]]: Simple but slow; updates all values at once using previous iteration values.
	- [[Gauss Seidel Method]]: Faster; updates each value as soon as it’s computed.
	- [[Successive Over-Relaxation]]: Even faster; uses a relaxation factor ω to speed up convergence.
- **Relaxation methods** further optimize the solution process by:
    - Avoiding direct matrix inversion.
    - Iteratively improving the guess until convergence.
    - Leveraging sparsity for faster updates.
### Analogy:
Think of solving the PDE as filling a giant puzzle:

- **Sparse matrices** reduce the size of the puzzle by ignoring unnecessary pieces.
- **Relaxation methods** solve the puzzle by starting with a rough guess and refining it, piece by piece, in a smart order to converge faster.