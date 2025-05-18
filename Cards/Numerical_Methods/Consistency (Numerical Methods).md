up:: [[Numerical Methods MOC]]
tags:: #Math 
# Consistency
- Does the method approximate the correct equation?
$$LTE=\frac{x_{exact}​(t+h)−x_{numerical}​(t+h)}{h}​→0$$
- A numerical method is **consistent** if its local truncation error (LTE) vanishes as the step size h→0.
- If we take a tiny step size h, the numerical solution should closely match the true solution.
	- The method should resemble a [[Taylor Series]] expansion of the exact solution.
- $x_{exact}$ is the true analytical solution of the [[ODE]] using calculus
- $x_{numerical}$ is the [[Numerical Methods MOC]] approximation
- $Error=x_{exact}​−x_{numerical}$
- 