up:: [[Numerical Methods MOC]]
tags:: #Math
# Secant Method
$$x_n = x_{n-1} - f(x_{n-1}) \cdot \frac{x_{n-1} - x_{n-2}}{f(x_{n-1}) - f(x_{n-2})}$$
- Uses two initial points and a secant line (linear approximation) to find the root.

- **Advantages**:
	- Faster convergence than bisection.
	- Avoids derivative calculations (unlike Newton’s method).

- **Disadvantages**:
	- May fail to converge if the initial points are poorly chosen.
	- Does not guarantee a root unless the function behaves well.

- **Application to Implied Volatility**:
	- Often used because it’s faster than bisection and doesn’t require derivatives, which can be expensive to compute numerically for Black-Scholes.

![[Pasted image 20250126205757.png]]