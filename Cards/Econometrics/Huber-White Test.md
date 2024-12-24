up:: [[Econometrics MOC]]
tags:: #Math
# Huber-White Test
- When you have White's [[Heteroskedasticity]]
	- No particular structure for errors, just not constant
	- Detected by [[White Test]]
## White Correction/White Robust Errors
- The test employs a correction to the standard errors, attempting to fix heteroskedasticity
- Changes the actual standard errors into *heteroskedasticity consistent errors (HCSE)*
	- Standard errors = $\hat{\beta}_{HC} = (X'X)^{-1} X' \Omega X (X'X)^{-1}$
		- 1. **β^​HC​**: This denotes the heteroskedasticity-consistent (robust) estimate of the variance-covariance matrix of the regression coefficients.
		-  **X**: This is the matrix of independent variables (also called the design matrix). It is an n×k matrix, where n is the number of observations and k is the number of predictors (including the intercept).
		- **X′**: This is the transpose of the matrix X. The transpose of an n×k matrix is a k×n matrix.
		- **X′X**: This is the product of the transpose of XX and XX itself. It is a k×kk×k matrix, where kk is the number of predictors.
		- **(X′X)−1**: This is the inverse of the X′X matrix. The inverse of a matrix A is denoted as A−1 and satisfies the property AA−1=I, where I is the identity matrix. [[Linear Algebra MOC]]
		- **Ω**: This is a diagonal matrix with the squared residuals on the diagonal. It accounts for the heteroskedasticity in the residuals. If u^i​ represents the residual for the ii-th observation, then ΩΩ is a diagonal matrix with elements u^i2u^i2​:
		- Ω=diag(u^12,u^22,…,u^n2)