up:: [[Linear Algebra MOC]]
tags:: #Math
# Cholesky Decomposition
- **Purpose:** to create correlated random variables for testing and simulation
- Is also the square root of a matrix
- Applicable to **symmetric, positive-definite** matrices
- It decomposes a matrix $A$ into the product of a lower triangular matrix $L$ and its transpose $L^T$:
$$ A = LL^T$$
## Example:

Consider the symmetric, positive-definite matrix $( A )$:

$A = \begin{pmatrix}4 & 12 & -16 \\12 & 37 & -43 \\-16 & -43 & 98\end{pmatrix}$


We want to decompose $( A )$ into the product of a lower triangular matrix $( L )$ and its transpose $( L^T )$, such that $( A = LL^T )$.

The steps for Cholesky decomposition are as follows:

1. Compute $( L_{11} )$:

	$L_{11} = \sqrt{4} = 2$

2. Compute $( L_{21} )$ and $( L_{31} )$:

	$L_{21} = \frac{12}{2} = 6$

	$L_{31} = \frac{-16}{2} = -8$


3. Compute $( L_{22} )$:

	$L_{22} = \sqrt{37 - 6^2} = \sqrt{1} = 1$

4. Compute $( L_{32} )$:

	$L_{32} = \frac{-43 - (6 \cdot 1)}{1} = -49$

5. Compute $( L_{33} )$:

	$L_{33} = \sqrt{98 - (-8)^2 - (-49)^2} = \sqrt{1} = 1$

Thus, the lower triangular matrix $( L )$ is:

	$L = \begin{pmatrix}2 & 0 & 0 \\6 & 1 & 0 \\-8 & -49 & 1\end{pmatrix}$


Verifying the decomposition:

$LL^T = \begin{pmatrix}2 & 0 & 0 \\6 & 1 & 0 \\-8 & -49 & 1\end{pmatrix}\begin{pmatrix}2 & 6 & -8 \\0 & 1 & -49 \\0 & 0 & 1\end{pmatrix} = \begin{pmatrix}4 & 12 & -16 \\12 & 37 & -43 \\-16 & -43 & 98\end{pmatrix} = A$

Thus, the Cholesky decomposition is confirmed.

## Valuation Worked Example
![[Pasted image 20241113164944.png]]

