up:: [[Linear Algebra MOC]]
tags:: #Math
# [[Covariance]] Matrix
$$\hat{\Sigma} = \frac{1}{m-1} (X - \bar{X})^T (X - \bar{X})$$

- Measures how much 2 or more variables change together
- Used commonly in [[Portfolio Theory MOC]] to measure the standard deviation of returns (risk)
	- ![[Pasted image 20240704132408.png]]


- Given a data matrix $X$ with $n$ variables and $m$ observations, where each column represents a variable and each row represents an observation, the sample covariance matrix $Σ$ can be calculated as:
	- $\Sigma = \mathbf{Cov}(\mathbf{X}) = \mathbb{E}[(\mathbf{X} - \mathbb{E}[\mathbf{X}])(\mathbf{X} - \mathbb{E}[\mathbf{X}])^T]$
		- where $E[X]$ is the expected value (mean) of the vector $X$.
## Properties
- **Symmetry:** The covariance matrix is symmetric, meaning $Σij​=Σji​$
- **Positive Semi-Definite:** The covariance matrix is positive semi-definite, which means that for any vector $a$: $aTΣa≥0$
	- [[Quadratic Forms]]

## Important Equations
- **Expected Value of a Linear Combination of Random Variables:**
	- $\mathbb{E}[\mathbf{w}'\mathbf{x}] = \mathbf{w}'\boldsymbol{\mu}$
	- Here, $w$ is a vector of weights, $x$ is a vector of random variables, and $μ$ is the vector of expected $v$
		- This is essentially a [[Multiple Linear Regression]]
		- The expected return of a portfolio is the weighted sum of the expected returns of individual assets, where the weights are the proportions of the portfolio invested in each asset.
		
- **Variance of a Linear Combination of Random Variables:**
	- $\text{Var}[\mathbf{w}'\mathbf{x}] = \mathbf{w}'\Sigma \mathbf{w}$
	- $Σ$ is the covariance matrix of the random variables $x$. The variance of the portfolio return is given by this [[Quadratic Forms]] involving the covariance matrix and the weight vector.
	
- **Covariance Between Two Linear Combinations of Random Variables:**
	- $\text{Cov}(\mathbf{w}'\mathbf{x}, \mathbf{v}'\mathbf{x}) = \mathbf{w}'\Sigma \mathbf{v}$
	- Same set of random variables $x$, where $w$ and $v$ are different vectors of weights.
	- This shows how the covariance of two portfolios (or any two linear combinations of the same set of assets) is *derived using their weight vectors* and the covariance matrix of the asset returns.
	
- [[Covariance Manipulations]]

## Some General Notes
- If all correlations are 0
	- variables are uncorrelated --> covariances are also 0
- Variance of the sum of the x values
	- Variance of sum = sum of variances
- Covariance between weighted sums: 
	- Product involving weighting vectors and the covariance matrix.
- What is the covariance (vector) between each individual $x$ and the sum of the $x$'s?
	- The covariance between an individual variable $x_i​$ and the sum $S$ of all variables is the sum of the covariances between $x_i$​ and each of the $x$ values.