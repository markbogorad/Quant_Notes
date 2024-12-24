up:: [[Calculus MOC]]
tags:: #Math
# Lagrange Multiplier
- A way to solve NLP problems in [[Optimization]]
- The basic idea behind Lagrange multipliers is **to transform a constrained optimization problem into an unconstrained one** by **incorporating the constraints into the objective function** using additional variables called Lagrange multipliers.
## Steps
1) Form the Lagrangian function
- $\mathcal{L}(x, y, \lambda) = \textcolor{green}{f(x, y)} + \lambda \left[ \textcolor{yellow}{g(x, y)} \right]$
	- Green --> original objective function
	- Blue --> Lagrangian multiplayer with constraint equation in brackets
	- $\lambda$ --> Lagrangian multiplier
	
2) Compute [[Partial Derivatives]] of $\mathcal{L}$ with respect to $x, y, \lambda$
- $\frac{∂x}{∂L}​=0,\frac{∂y}{∂L}​=0,\frac{∂λ}{∂L}​=0$

3) Solve the system of equations that satisfies all values of $x, y, \lambda$

## Example
Suppose we want to maximize the function $( f(x, y) = x + y )$ subject to the constraint $( x^2 + y^2 = 1 )$

- **Form the Lagrangian**
$\mathcal{L}(x, y, \lambda) = x + y + \lambda (1 - x^2 - y^2)$

- **Compute Partial Derivatives**
$\frac{\partial \mathcal{L}}{\partial x} = 1 - 2\lambda x = 0 \quad \Rightarrow \quad 1 = 2\lambda x \quad \Rightarrow \quad \lambda = \frac{1}{2x}$

$\frac{\partial \mathcal{L}}{\partial y} = 1 - 2\lambda y = 0 \quad \Rightarrow \quad 1 = 2\lambda y \quad \Rightarrow \quad \lambda = \frac{1}{2y}$

$\frac{\partial \mathcal{L}}{\partial \lambda} = 1 - x^2 - y^2 = 0 \quad \Rightarrow \quad x^2 + y^2 = 1$

- **Solve the System of Equations**

- From $( \lambda = \frac{1}{2x} ) and ( \lambda = \frac{1}{2y} )$, we get:
$\frac{1}{2x} = \frac{1}{2y} \quad \Rightarrow \quad x = y \quad \text{or} \quad x = -y$

- **Using the constraint $( x^2 + y^2 = 1 )$:**

1. If $( x = y )$:
$x^2 + x^2 = 1 \quad \Rightarrow \quad 2x^2 = 1 \quad \Rightarrow \quad x = \pm \frac{1}{\sqrt{2}}$

2. If $( x = -y )$:
$x^2 + (-x)^2 = 1 \quad \Rightarrow \quad 2x^2 = 1 \quad \Rightarrow \quad x = \pm \frac{1}{\sqrt{2}}$

**Thus, the solutions are:**

$(x, y) = \left( \frac{1}{\sqrt{2}}, \frac{1}{\sqrt{2}} \right), \left( -\frac{1}{\sqrt{2}}, -\frac{1}{\sqrt{2}} \right), \left( \frac{1}{\sqrt{2}}, -\frac{1}{\sqrt{2}} \right), \left( -\frac{1}{\sqrt{2}}, \frac{1}{\sqrt{2}} \right)$

- These are all the optimized points

## What is Lambda?
- Think of it as the shadow cost of the constraint --> how much it will cost to incrementally loosen a constraint variable