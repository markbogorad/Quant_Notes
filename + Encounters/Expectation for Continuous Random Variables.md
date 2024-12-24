up:: [[Probability MOC]]
tags:: #Math
# Expectation for Continuous Random Variables
- For a [[Continuous Random Variables]] X with a [[Probability Density Function (PDF)]] $fX(x)$, the expected value of $X$ is calculated using the following integral:
$$E[X] = \int_{-\infty}^{\infty} x \cdot f_X(x) \, dx$$
- $x$: This represents the values that the random variable X can take.
- $fX(x)$: This is the probability density function, which describes the likelihood of XX taking on a particular value xx.
- $x⋅fX(x)$: This product gives the contribution to the expected value from each possible value of X, weighted by how likely that value is.
## Variance
$$\text{Var}(X) = E\left[(X - \mu)^2\right] = \int_{-\infty}^{\infty} (x - \mu)^2 \cdot f_X(x) \, dx$$
	$\text{Alternatively,}$
	
$$\text{Var}(X) = E[X^2] - (E[X])^2 = \int_{-\infty}^{\infty} x^2 \cdot f_X(x) \, dx - (\int_{-\infty}^{\infty} x \cdot f_X(x) \, dx)^2$$
