up:: [[Numerical Methods MOC]]
tags:: #Math
# Brent Method
- Combines [[Bisection Method]], [[Secant Method]], and inverse quadratic interpolation to find the root.
- It chooses the most efficient method adaptively at each iteration.

**Advantages**:
- Fast convergence similar to secant (almost as fast).
- Robust and does not “get lost” like Newton or Secant methods.

**Disadvantages**:
- More complex to implement.

**Application to [[Implied Volatility]]**:
- Preferred in practice because it combines robustness with speed. Used in numerical libraries for root-finding problems.