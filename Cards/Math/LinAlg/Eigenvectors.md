up:: [[Linear Algebra MOC]]
tags:: #Math
# Eigenvectors
- *Intuition*: A vector that stays on it's own span during a transformation (3blue1brown)
	- Gives the direction of the [[Eigenvalues]], i.e. the direction of the variance of the square matrix
- An eigenvector of a square matrix $A$ is a non-zero vector $v$ such that when $A$ multiplies $v$, the result is a scalar multiple of $v$ (this part is what staying on its own span refers to). 
	- This can be expressed as: $Av=λv$
		- $\lambda$ is the [[Eigenvalues]] corresponding to vector v
			- This indicates by how much the vector has stretched or shrunk
- **Key:** there is no directional change, only a stretch or shrink

## To Find Eigenvalues and Eigenvectors
- Simple formula (3blue1brown)
	- $\lambda = m \pm \sqrt{m^2-p}$
		- m = average of the diagonal elements
		- p = [[Matrix Determinant]]

- Traditional method
	- $\text{det}(A - \lambda I) = 0$
		- I = identity matrix
		- det = [[Matrix Determinant]]
	- Solution to this is [[Eigenvalues]]
		- Once the eigenvalues are known, substitute each $λ$ back into the equation $(A - \lambda I) = 0$ to find the corresponding eigenvectors $v$.

### Example:

**Given the matrix:**

		$A = \begin{pmatrix} 4 & 1 \\ 2 & 3 \end{pmatrix}$

1. **Calculate $( m )$:**

		$m = \frac{4 + 3}{2} = \frac{7}{2} = 3.5$

2. **Calculate $( p )$:**

		$p = \frac{(4 - 3)^2 + 4 \cdot 1 \cdot 2}{4} = \frac{1 + 8}{4} = \frac{9}{4} = 2.25$

3. **Compute the eigenvalues:**

		$\lambda = m \pm \sqrt{m^2 - p}$
		
		$\lambda = 3.5 \pm \sqrt{3.5^2 - 2.25}$
		
		$\lambda = 3.5 \pm \sqrt{12.25 - 2.25}$
		
		$\lambda = 3.5 \pm \sqrt{10}$
		
		$\lambda = 3.5 \pm 3.162$

**So the eigenvalues are:**

	$\lambda_1 = 3.5 + 3.162 = 6.662$
	$\lambda_2 = 3.5 - 3.162 = 0.338$

