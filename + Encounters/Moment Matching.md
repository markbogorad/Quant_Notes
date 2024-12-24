up:: [[Quantitative Valuation MOC]]
tags:: #Finance  
# Moment Matching
- Matching the statistical properties (mean, var, skewness) of the simulated sample closely matches the theoretical distribution
	- Forcing moments to equal what you want them (i.e. imposing $\mu=0$, $\sigma=1$)
- Needs a large sample size to work well
- Can increase convergence speed
- Reduces discrepancies between simulated variables and actual
## How it works
- Replace the z values with their standardized equivalent by subtracting by the mean and dividing by the variance
	- Ex: make a normal sample a standard normal by [[Standardization]], i.e. $\frac{X-\bar{X}}{SD(X)}=X^*$
- **More serious approach** (Joaquin)
	- For multivariate: calculate the [[Covariance Matrix]] and then the [[Cholesky Decomposition]]
$$\left( X - \overline{X} \frac{1}{n} \right) \cdot \left( C^T \right)^{-1} = X^*$$
