up:: [[Linear Algebra MOC]]
tags:: #Math
# Rank
- The maximum number of *linearly independent* rows or columns in the matrix
	- Tells you the dimension of the column (or row) space
- Tells you if solutions exist to the system of linear equations ([[Matrices as a System of Linear Equations]])
	- **Consistent System**: If the rank of the *augmented matrix* $[A∣b]$ is equal to the rank of *the coefficient matrix* $A$, the system is consistent (has at least one solution).
	- **Inconsistent System**: If the rank of the augmented matrix is greater than the rank of the coefficient matrix, the system is inconsistent (has no solutions).
	- If the rank of the matrix $A$ is **equal to the number of unknowns**, the system has a unique solution.
    - If the rank of the matrix $A$ is **less than the number of unknowns**, the system has infinitely many solutions.
- **Full Rank Matrix**
	- A $3×3$ matrix with rank 3 means all rows (and columns) are linearly independent, and the matrix is invertible.
- **Rank-Deficient Matrix**
	- A $4×5$ matrix with rank 3 means there are 3 linearly independent rows (or columns), and the system of equations it represents might have infinitely many solutions or no solution depending on the augmented matrix.

## Properties of Matrix Rank
1. **Non-Negative:** The rank of a matrix is always a non-negative integer.
2. **Rank of Zero Matrix:** The rank of a zero matrix (all elements are zero) is 0.
3. **Rank and [[Matrix Multiplication]]:** If $A$ is an $m×n$ matrix and $B$ is an $n×p$ matrix, then: $rank(AB)≤min⁡(rank(A),rank(B))$
4. **Full Rank:** A matrix is said to have full rank if its *rank is equal to the smallest dimension of the matrix*. For example, an $m×n$ matrix $A$ has full rank if $rank(A)=min⁡(m,n)$.

## To Find the Rank
- Need to transform the matrix into it's reduced row echelon form (RREF)
	- To find RREF
	1) Set a pivot element: a non-zero element used to eliminate other elements in it's column
		- These are on the diagonal (first row, first element... then 2nd row, 2nd element) --> as long as its not 0
	2) Preform row operations
		- Swapping two rows.
		- Multiplying a row by a non-zero scalar.
		- Adding or subtracting a multiple of one row to another row, multiple comes from step above
- Unusual method, see example
#### Example:
**Goal:** you are trying to manipulate the matrix to get as many zeros as possible (this is called Gaussian Elimination)

Consider the matrix $A$:

$A = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{pmatrix}$

To find the rank, we perform row operations to **convert $A$ to its row echelon form:**
1. Subtract 4 times the first row from the second row. --> will make $A_{2,1} = 0$
2. Subtract 7 times the first row from the third row. --> will make $A_{3,1} = 0$

Becomes:
$\begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & -6 & -12 \end{pmatrix}$

Next, divide the second row by -3, this standardizes the -3 in row 2 to 1 for further operations:
$\begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & -6 & -12 \end{pmatrix}$ = $\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 2 \\ 0 & -6 & -12 \end{pmatrix}$

Finally, now that the 2nd element in row 2 is 1, add 6 times the second row to the third row, this gets more zeros:
$\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 2 \\ 0 & -6 & -12 \end{pmatrix}$ = $\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 2 \\ 0 & 0 & 0 \end{pmatrix}$

The row echelon form of A **has 2 non-zero rows**, so the rank of $A$ is 2.
