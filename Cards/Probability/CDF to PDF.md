up:: [[Probability MOC]]
tags:: #Math 
# CDF to PDF
$$F(x) = P(X \leq x) = f(x) = \frac{d}{dx} F(x)$$
- Easiest way to think of this is undoing the CDF by reversing taking the area under the curve (integrating)
## Ex: exponential distribution
- $F(x) = 1 - e^{-\lambda x}$ for $x \geq 0$ for $x < 0$
- $f(x) = \frac{d}{dx} F(x) = \lambda e^{-\lambda x} \text{for } x \geq 0 \text{for } x < 0$