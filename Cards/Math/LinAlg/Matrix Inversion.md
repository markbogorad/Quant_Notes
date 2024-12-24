up:: [[Linear Algebra MOC]]
tags:: #Math
# Matrix Inversion
- Only works on square matrices that have a non zero determinant
	- If no inverse, it is called non-invertible
- When the inverse matrix is multiplied by the original matrix, you get the identity matrix (see: [[Matrices]])
-  The inverse of $(A) = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$ is $(A)^-1 = \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$
- For larger matricies:
	- ![[Pasted image 20240703170216.png]]
- For even larger you need to do **Gaussian elimination**
## Properties of the Inverse
- Inverse of a product: $(AB)^{-1} = B^{-1} A^{-1}$
- Inverse of a transpose: $(A^T)^{-1} = (A^{-1})^T$
- Inverse of an inverse: $(A^{-1})^{-1} = A$

## Gauss-Jordan Elimination (Row Operations)
- Transform given matrix into the identity matrix
- Apply more operations to identity matrix to get inverse matrix
- Original matrix --> identity matrix --> inverse matrix
### How it works in practice
- Make an augmented matrix and slowly shift over the identity matrix to the other side with row operations
- $A = \begin{pmatrix} 2 & 1 \\ 5 & 3 \end{pmatrix}$ --> $[A | I] = \begin{pmatrix} 2 & 1 & | & 1 & 0 \\ 5 & 3 & | & 0 & 1 \end{pmatrix}$ 
- $R1 \rightarrow \frac{1}{2} R1 \begin{pmatrix} 1 & \frac{1}{2} & | & \frac{1}{2} & 0 \\ 5 & 3 & | & 0 & 1 \end{pmatrix}$ $R2 \rightarrow R2 - 5R1 \begin{pmatrix} 1 & \frac{1}{2} & | & \frac{1}{2} & 0 \\ 0 & \frac{1}{2} & | & -\frac{5}{2} & 1 \end{pmatrix}$ 
- $R2 \rightarrow 2R2 \begin{pmatrix} 1 & \frac{1}{2} & | & \frac{1}{2} & 0 \\ 0 & 1 & | & -5 & 2 \end{pmatrix}$ $R1 \rightarrow R1 - \frac{1}{2}R2 \begin{pmatrix} 1 & 0 & | & 3 & -1 \\ 0 & 1 & | & -5 & 2 \end{pmatrix}$ 
- Inverse has become: $A^{-1} = \begin{pmatrix} 3 & -1 \\ -5 & 2 \end{pmatrix}$
