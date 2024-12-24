up:: [[Linear Algebra MOC]]
tags:: #Math
# Matrix
$$A = \begin{pmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{pmatrix}$$
- Array of numbers sorted in rows and columns
## Key Matrix Features
- **Symmetric Matrix**
	- A matrix is symmetric if it is equal to it's **transpose**, which means $a21=a12$​. 
		- The elements on the off-diagonals are equal.
	- $\text{Symmetric if } a_{21} = a_{12}$
	
- **Transpose (denoted by ')**
	- The transpose of a matrix $A$ is obtained by swapping its rows with its columns.
	- $A^T = A' = \begin{pmatrix} a_{11} & a_{21} \\ a_{12} & a_{22} \end{pmatrix}$
		- Notice $a_{12}$ is now $a_{21}$
	
- **Identity Matrix**
	- The identity matrix is a square matrix with ones on the main diagonal and zeros elsewhere. It acts as the multiplicative identity for matrices.
		- A diagonal matrix that also has 1s on the diagonal itself
	- $I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$

- **Diagonal Matrix**
	- A diagonal matrix is a matrix in which the entries outside the main diagonal are all zero. For a matrix $A$:
	- $\text{Diag}(A) = \begin{pmatrix} a_{11} & 0 \\ 0 & a_{22} \end{pmatrix}$

- **Lower Diagonal Matrix**
	- A lower triangular matrix (also known as a lower diagonal matrix) has *all elements above the main diagonal equal to zero.*
	- Used for decomposition of a matrix ([[Cholesky Decomposition]], [[Schur Complement]])
	- $A = \begin{pmatrix} a_{11} & 0 \\ a_{21} & a_{22} \end{pmatrix}$

- **Trace**
	- The trace of a matrix is the sum of its diagonal elements.
	- $\text{tr}(A) = a_{11} + a_{22}$
	
- Leading Principal Minor
	- a [[Matrix Determinant]] of a submatrix that is located in the top-left corner of the original matrix.
	- For a 3x3 matrix
		- Order 1 leading principle minor: $a_{11}$
		- Order 2 leading principle minor --> determinant of the 2x2 inside: $a_{11}a_{22}-a_{12}a_{21}$
		- Order 3: regular determinant
	
- [[Matrix Rank]]

