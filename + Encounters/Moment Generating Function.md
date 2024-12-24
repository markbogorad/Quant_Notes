up:: [[Probability MOC]]
tags:: #Math 
# Moment Generating Function
- Used when [[Expectation]], [[Variance]], [[Covariance]] are not easily computed with their formulas - i.e. you have wierd formulas for your CDF
$$\mathbb{E}(X^n) = M_X^{(n)}(0) = \frac{d^n}{dt^n} M_X(t) \bigg|_{t=0}$$
- The first derivative $M_X^{′}​(0)$ gives $E(X)$ (the mean).
- The second derivative $M_X^{′′}(0)$ gives $E(X^2)$.
- The third derivative $M_X​^{′′′}(0)$ gives $E(X^3)$, and so on.

**Expectation**:
- $\mathbb{E}(X) = M_X'(0)$
**Variance**
- $\text{Var}(X) = M_X''(0) - \left( M_X'(0) \right)^2$
**Covariance**
- $\text{Cov}(X, Y) = \frac{\partial^2}{\partial s \, \partial t} M_{X,Y}(s, t) \bigg|_{s=0, t=0} - M_X'(0) M_Y'(0)$
