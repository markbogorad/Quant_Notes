up:: [[Risk Management MOC]]
tags:: #Finance 
# Monte Carlo VaR
- Simulation VaR metod
	- Step 5 - covariance matrix decomposition
		- Either eignen decomposition or choelsky here
			- Eigenvalue/eigenvector is better because Cholesky requires an _ type of matrix
				- $\Sigma = E \Lambda E'$ - eigen decomp
					- If you do this, you get correlated random variables
					- $\Lambda^{1/2} E$ - prism

- Assume a distribution, simulate stochastic paths on that distribution
- Only requirement is that your distribution is accurate, everything else falls into place
## Pros
- Good for path dependent and convex portfolios
## Cons
- Assumption of the distribution is risky and can trickle down into moments (skewness, curtosis)
## Steps
1. Random uniform number generation
2. Random normal conversion
3. Covariance matrix generation
4. Covariance matrix factorization - getting square root ([[Cholesky Decomposition]] or [[Eigenvalue Decomposition]])
5. Creation of correlated random “shock” variables
6. Use of shocks for repricing, hypothetical P&L
7. Estimating the VaR

- ![[Screenshot 2025-03-19 at 12.25.25 PM.png]]