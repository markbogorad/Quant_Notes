up:: [[Linear Algebra MOC]]
tags:: #Math
# [[Derivatives]] of Matrices
- With respect to a scalar:
	- Derive each element of the matrix with respect to the scalar
		- $\frac{dX}{dt} = \begin{pmatrix} \frac{df_{11}(t)}{dt} & \frac{df_{12}(t)}{dt} \\ \frac{df_{21}(t)}{dt} & \frac{df_{22}(t)}{dt} \end{pmatrix}$
		- Ex:
			- $X = \begin{pmatrix} t^2 & \sin(t) \\ \cos(t) & e^t \end{pmatrix}$    becomes    $\frac{dX}{dt} = \begin{pmatrix} 2t & \cos(t) \\ -\sin(t) & e^t \end{pmatrix}$

- Derivative of a [[Quadratic Forms]]
	- $\nabla_{\mathbf{x}} (\mathbf{x}^T A \mathbf{x}) = 2A \mathbf{x}$
	- Solved by:
		- $Q = (x \quad y) \begin{pmatrix} a & b \\ b & c \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix} = ax^2 + 2bxy + cy^2$
		- $\frac{dQ}{d\vec{x}} = \begin{pmatrix} 2ax + 2by \\ 2bx + 2cy \end{pmatrix} = 2\begin{pmatrix} a & b \\ b & c \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix}$
	


