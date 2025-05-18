up:: [[Quantitative Valuation MOC]]
tags:: #Finance  
# Antithetic Variance Reduction
- For each random variable $U$ that you create, you also create it's antithetic (antithesis) counterpart $(1-U)$
	- Basically doubling sample size by including negative counterparts
	- These balance each other out and reduce total variance
	- The idea is that if $f$ is a monotonic function, then $f(U)$ and $f(1-U)$ will vary in opposite directions
- This forces mean to be 0
- Creates negative correlations which reduce overall variance
## Example: exponential simulation
- For example, with a sample of $( X \sim N(0, 1) )$, we want to estimate $( V = \mathbb{E} \left[ e^X \right] )$. Instead of just using $( \hat{V} = \frac{1}{n} \sum_{i} e^{x_i} )$, we can generate the antithetic version $( Y = -X )$ such that
$$V = \mathbb{E} \left[ \frac{e^X + e^{-X}}{2} \right] = \frac{1}{2} \left( e^{1/2} + e^{1/2} \right) = e^{1/2} = \mathbb{E} \left[ e^X \right]$$
- See X is averaged with a -X
  $$\text{Var} \left( \frac{e^X + e^{-X}}{2} \right) = \frac{1}{4} \left[ \text{Var}(e^X) + \text{Var}(e^{-X}) + 2 \, \text{Cov}(e^X, e^{-X}) \right] = \frac{1}{2} \left[ \text{Var}(e^X) + \text{Cov}(e^X, e^{-X}) \right]$$
  
