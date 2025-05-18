up:: [[Numerical Methods MOC]]
tags:: #Math
# Newtons Method
$$x_n = x_{n-1} - \frac{f(x_{n-1})}{f'(x_{n-1})}$$
- a fixed-point iteration method that uses the function’s derivative for a quadratic convergence rate.
	- The tangent at $x_{n−1}$ is used to approximate the root.
	
- **Advantages**:
	- Very fast convergence (quadratic) when close to the root.
	- Reduces the number of iterations dramatically compared to other methods.

- **Disadvantages**:
	- Requires computing $f′(x)$, which might be complex for implied volatility.
	- Can diverge if the initial guess is far from the root.

- **Application to [[Implied Volatility]]**:
	- Used when derivatives (like the [[Vega]] of the option in Black-Scholes) can be efficiently calculated. It’s often combined with other methods for better robustness.

![[Pasted image 20250126205808.png]]