up:: [[Linear Algebra MOC]]
tags:: #Math
# Hessian Matrix
$$\begin{bmatrix}
\frac{\partial^2 f}{\partial x_1^2} & \frac{\partial^2 f}{\partial x_1 \partial x_2} & \cdots & \frac{\partial^2 f}{\partial x_1 \partial x_n} \\
\frac{\partial^2 f}{\partial x_2 \partial x_1} & \frac{\partial^2 f}{\partial x_2^2} & \cdots & \frac{\partial^2 f}{\partial x_2 \partial x_n} \\
\vdots & \vdots & \ddots & \vdots \\
\frac{\partial^2 f}{\partial x_n \partial x_1} & \frac{\partial^2 f}{\partial x_n \partial x_2} & \cdots & \frac{\partial^2 f}{\partial x_n^2}
\end{bmatrix}$$
- A square matrix of **second-order** [[Partial Derivatives]] of a scalar-valued function
- Used in [[Constrained Optimization]] to asses the curvature of the function being optimized 
	- The Hessian is used to determine the nature of critical points. 
		- If positive definite at a point, the function has a *local minimum there;* 
		- if negative definite, the function has a *local maximum;* 
		- if it is indefinite, the point is a *saddle point.*
