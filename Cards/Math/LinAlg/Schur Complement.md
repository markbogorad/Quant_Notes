up:: [[Linear Algebra MOC]]
tags:: #Math
# Schur Complement
- Shows how 1 element of the matrix interacts with the others
### Example:
- Let's say you have a 2x2 matrix like this:
	- $M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$
- The Schur Complement of $D$ would be
	- $d = a - \frac{b \cdot c}{d}$
- Let's take an example where $(a = 4)$, $(b = 2)$, $(c = 1)$, and $(d = 3)$. 
	- Using the formula: $\text{Schur complement of } d = 4 - \frac{2 \cdot 1}{3} = 4 - \frac{2}{3} = 4 - 0.67 = 3.33$ 
		- So, the Schur complement of $(d)$ in this matrix is $(3.33)$.