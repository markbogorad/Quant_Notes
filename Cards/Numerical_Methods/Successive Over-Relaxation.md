up:: [[Numerical Methods MOC]]
tags:: #Math 
# Successive Over Relaxation
$$x_i^{(k+1)} = (1 - \omega) x_i^{(k)} + \omega \cdot \frac{1}{A_{ii}} \left( b_i - \sum_{j < i} A_{ij} x_j^{(k+1)} - \sum_{j > i} A_{ij} x_j^{(k)} \right)$$
- An improvement over [[Gauss Seidel Method]] by introducing a relaxation factor ω to accelerate convergence.
- $ω∈(0,2)$:
	- $ω=1$: Gauss-Seidel
	- $ω>1$: Over-relaxation (faster convergence)
	- $ω<1$: Under-relaxation (stabilizes when convergence is slow)
