up:: [[Linear Algebra MOC]]
tags:: #Math 
# Quadratic Forms
- A quadratic form in $n$ variables $x1,x2,…,xn​$ can be written as: $Q(x)=∑_{i=1}^n∑_{j=1}^na_{ij}x_ix_j$ where $a_{ij}$​ are constants.
	- Made simpler: 
		- For a vector $x∈Rn$ and a symmetric matrix $A∈Rn×n$, 
		- the quadratic form $Q(x)$ is given by: 
			- $Q(x)=x^TAx$ 
				- where
					- $x$ is a column vector
					- $x^T$ is its transpose
					- $A$ is a symmetric matrix
## Example:
Consider a quadratic form in two variables $x1​$ and $x2$​:      $Q(x1,x2)=3x_1^2+2x_1x_2+x_2^2$​

This can be represented in matrix form as:        $\begin{pmatrix} x_1 & x_2\end{pmatrix}$ $\begin{pmatrix} 3 & 1 \\ 1 & 1 \end{pmatrix}$$\begin{pmatrix} x_1 \\ x_2 \end{pmatrix}$

## Properties of Quadratic Forms
- Symmetry
	- The matrix $A$ in the quadratic form $Q(x)=x^TAx$ is symmetric, i.e., $A=A^T$.
	
- Definiteness: A quadratic form $Q(x)$ can be classified based on the definiteness of the matrix $A$:
	- **Positive Definite:** If $Q(x)>0$ for all $x≠0$
	- **Positive Semidefinite:** If $Q(x)≥0$ for all $x$.
	- **Negative Definite:** If $Q(x)<0$ for all $x≠0$.
	- **Negative Semidefinite:** If $Q(x)≤0$ for all $x$.
	- **Indefinite:** If $Q(x)$ takes both positive and negative values.
	
- [[Eigenvalues]]
	- **Positive definite** if all eigenvalues of $A$ are positive.
	- **Positive semidefinite** if all eigenvalues of $A$ are non-negative.
	- **Negative definite** if all eigenvalues of $A$ are negative.
	- **Negative semidefinite** if all eigenvalues of $A$ are non-positive.
	- **Indefinite** if $A$ has both positive and negative eigenvalues.

## Example Calculation
Let's compute a quadratic form for a given vector and matrix:

$\mathbf{x} = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$ , $A = \begin{pmatrix} 3 & 1 \\ 1 & 1 \end{pmatrix}$

	$Q(\mathbf{x}) = \mathbf{x}^T A \mathbf{x}$

		$\mathbf{x}^T = \begin{pmatrix} 1 & 2 \end{pmatrix}$

			$Q(\mathbf{x}) = \begin{pmatrix} 1 & 2 \end{pmatrix} \begin{pmatrix} 3 & 1 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix}$

			$Q(\mathbf{x}) = \begin{pmatrix} 1 & 2 \end{pmatrix} \begin{pmatrix} 3 \cdot 1 + 1 \cdot 2 \\ 1 \cdot 1 + 1 \cdot 2 \end{pmatrix} = \begin{pmatrix} 1 & 2 \end{pmatrix} \begin{pmatrix} 5 \\ 3 \end{pmatrix} = Q(\mathbf{x}) = \begin{pmatrix} 1 & 2 \end{pmatrix} \begin{pmatrix} 5 \\ 3 \end{pmatrix} = 1 \cdot 5 + 2 \cdot 3 = 11$
	
- [[Matrix Multiplication]]

## Using Quadratic Forms to get portfolio variance
- In practice: this is how you find the variance of a portfolio ([[Portfolio Theory MOC]])
- Portfolio with $n$ assets can be expressed as:
	- $\sigma_p^2 = \mathbf{w}^T \Sigma \mathbf{w}$
	- where:
		- $w$ is the vector of portfolio weights, where $wi$​ represents the proportion of the total portfolio value invested in asset $i$.
		- $\sum$ is the [[Covariance Matrix]] of the asset returns, where $σ_{ij​}$ represents the covariance between the returns of assets $i$ and $j$.
	- **Portfolio variance** is given by : $\sigma_p^2 = \begin{pmatrix} w_1 & w_2 \end{pmatrix} \begin{pmatrix} \sigma_{11} & \sigma_{12} \\ \sigma_{21} & \sigma_{22} \end{pmatrix} \begin{pmatrix} w_1 \\ w_2 \end{pmatrix}$
