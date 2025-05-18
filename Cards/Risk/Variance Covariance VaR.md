up:: [[Risk Management MOC]]
tags:: #Finance 
# Variance Covariance VaR
- Need variances and covariances of everything
	- You basically spam this for every combination: variance of **$(xa+yb) =x^2var(a)+y^2var(b)+2xycov(ab)$**
- Covariance - how much and which direction x moves when y moves 
	- how much 1 variable moves after shifting another variable by a unit
	- Correlation is scaled covariance used to make everything one unit (covariance is not unit free)
		- Units are important in FX with different denominations
- Need to weight past observations:
	- Exponentially, unweighted, or with GARCH
-  - X'VX
		- X position matrix 
		- v is covariance matrix (quadratic form) = variance of portfolio (sqrt of this is std, * 2.33 gives portfolio VaR)
		- 4 years has good sample size properties - 1000 observations roughly and 1% VaR would be 10 observations
		- `Small` function rankest smallest obs in excel


![[Screenshot 2025-03-19 at 12.04.55 PM.png]]