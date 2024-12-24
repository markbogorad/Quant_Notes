up:: [[Linear Algebra MOC]]
tags:: #Math 
# Gradients
- Imagine you are hiking on a hill. The height of the hill at any point can be described by a function $f(x,y)$, where $x$ and $y$ are your coordinates on the ground.
- The gradient of the function $f$, often written as $∇f$, is like an arrow pointing in the direction where the hill is the steepest uphill. If you follow this arrow, you'll be climbing up the hill as quickly as possible.
- The length of this arrow tells you how steep the hill is in that direction. A longer arrow means the hill is steeper, while a shorter arrow means it is less steep.

## How to Find the Gradient
- To find the gradient, you calculate how much the height $f(x,y)$ changes as you move a little bit in the $x$ direction and a little bit in the $y$ direction. These changes are [[Partial Derivatives]]
	- For a function $f(x,y)$, the gradient is: $∇f(x,y)=(\frac{∂f}{∂x},\frac{∂f}{∂y})$

## Gradient of Vector Valued Functions
- A vector-valued function takes a vector as input and produces another vector as output
- The gradient of a vector valued function is a [[Jacobian Matrices]]
	- A grid of [[Partial Derivatives]] 
	- Tells you how the output vector of a function changes as you move around in the input space