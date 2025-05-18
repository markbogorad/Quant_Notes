up:: [[Numerical Methods MOC]]
tags:: #Math 
# Linear vs Non-Linear
- Most equations in finance are linear
## Linear PDE
A [[PDE]] is linear if:
- The unknown function and its partial derivatives appear only to the first power.
- There are **no products** or nonlinear functions (e.g., sine, exponential) **of the unknown function** and its partial derivatives.
	- Basically $u$ and its derivatives appear linearly - meaning that derivatives appear seperately or $u$ is multiplied by a constant
$$a(x,y) \frac{\partial u}{\partial x} + b(x,y) \frac{\partial u}{\partial y} + c(x,y) u = d(x,y)$$
- $u$ is the unknown function
- $a,b,c$ are the known functions
- Examples: [[Heat Equation]], Wave Equation
## Non Linear PDE
A [[PDE]] is non linear if
- The unknown function or its derivatives are raised to a power other than 1.
- There are products of the unknown function or its derivatives.
- Non-linear functions (e.g., exponential, sine, cosine) involve the unknown function or its derivatives.
$$F\left(x,y,u,\frac{\partial u}{\partial x},\frac{\partial u}{\partial y}, \dots \right) = 0$$
- Examples: Navier Stokes, Non-linear Schrodinger
