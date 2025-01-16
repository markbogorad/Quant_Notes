up:: [[Quantitative Valuation MOC]]
tags:: #Finance  
# Correlating Cash Flows
- For simulating many different variables simultaneously
	- Can't just do this because **correlations need to be considered**
## How its done
- Start form an uncorrelated dataset of [[Standardization]] normal variables
- Simple case: you have numbers $z_1$ and $z_2$ with a correlation $\rho$. 
	- Begin with 2 independent random numbers $z_1$ and $z_3$
	- Compute $z_2$ as a linear combination of $z_1$ and $z_3$
		- To do this, we need
			1) mean of $z_2$ must be 0
			2) variance of $z_2$ must be 1
			3) Correlation between $z_1$ and $z_2$ must be $\rho$
		- These are all met by: $z_2 = \rho z_1 + z_3 \sqrt{1-\rho^2}$
		- In matrix form:
$$\begin{pmatrix} z_1 & z_2 \end{pmatrix} = \begin{pmatrix} z_1 & z_3 \end{pmatrix} \begin{pmatrix} 1 & \rho \\ 0 & \sqrt{1 - \rho^2} \end{pmatrix}$$
- Where
	- $\begin{pmatrix} z_1 & z_3 \end{pmatrix}$ is the uncorrelated data
	- $\begin{pmatrix} z_1 & z_2 \end{pmatrix}$ is the correlated result
	- $\begin{pmatrix} 1 & \rho \\ 0 & \sqrt{1 - \rho^2} \end{pmatrix}$ is the transpose of the lower diagonal [[Cholesky Decomposition]] of the [[Correlation Matrix]] $\begin{pmatrix} 1 & \rho \\ \rho & 1 \end{pmatrix}$
## Alt method
- Generate a random standard Gaussian sample Z
	- [[Creating Z Values (Inverse CDF)]]
- Use [[Moment Matching]] to obtain a sample with 0 mean and variance independent sample
	- Done by
	1) Compute average $\bar{Z}$ and the covariance matrix $\Sigma_{Z}$
	2) Compute [[Cholesky Decomposition]] matrix $C_z$
	3) Compute the standardized sample as $Z^* = (Z-\bar{Z}\mathbf{1}_n) \times (C_Z^T)^{-1}$
- Compute the desired correlation matrix with target correlations and it's [[Cholesky Decomposition]] $(C_{target})$
- Multiply the sample with the transpose of the desired Cholesky target 
	- $Z_{target} = Z^* \times C_{target}^T$
- Make the sample uniformly distributed
	- $u = N(Z_{target})$
- Use the inverse [[Cumulative Distribution Function (CDF)]] to convert into any analytical distribution
	- $X=CDF^-1(u)$

## Correlating Cashflows for Non Normal Variables
- Use [[Copulae (Simulation)]]