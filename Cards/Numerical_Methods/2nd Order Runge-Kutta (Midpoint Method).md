up:: [[Numerical Methods MOC]]
tags:: #Math
# Midpoint Method
- A second-order numerical method and a [[Runge-Kutta Methods]]
$$y_{n+1}=y_n+h⋅f(x_n+\frac{h}{2},y_n+\frac{h}{2}⋅f(x_n,y_n))$$
- Looking at a [[Taylor Series]] of a function $g(t_n)$ and adding a small step h
- An improvement above [[Eulers Method]] by taking a midpoint (intermediate step) and using the slope (derivative) at that midpoint
	- Basically countering the issue with [[Explicit Euler]] convergence for big step sizes because this captures slope in between
## The algorithm
- Compute midpoint estimate} $k_1 = h f(x_n, t_n)$ 
- Use $( k_1 )$ to estimate $( x )$ at the midpoint: $x_n + \frac{k_1}{2}, \quad t_n + \frac{h}{2}$ 
- Compute the final update using the slope at the midpoint: $x_{n+1} = x_n + h f\left( x_n + \frac{k_1}{2}, t_n + \frac{h}{2} \right)$ 
- If using a step size of $( 2h )$, an alternative formulation is: $x_{n+1} = x_{n-1} + 2h f(x_n, t_n) + O(h^3)$ 
- This method provides second-order accuracy, meaning the error is $( O(h^2) )$, making it more precise than Euler’s method.
## Visually
![[Pasted image 20250128140227.png]]

