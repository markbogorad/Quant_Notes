up:: [[Numerical Methods MOC]]
tags:: #Math
# Explicit Euler
- Provides an approximate solution to [[ODE]] by using the **current value** of the function and its derivative to predict the next value.
	- Approximate using [[Taylor Series]]
$$x_{n+1}​=x_n​+hf(x_n​,t_n​)$$
- $x_n$​ is the current approximation at $t_n​$
- $x_{n+1}$ is the approximation at $t_{n+1}=t_n+h$
- $f(x_n​,t_n​)$ is the derivative evaluated at $(x_n​,t_n​)$.
	- $\frac{dt}{dx}​=f(x,t)$
- $h$ is the step size.
- Formula is current approximation + step size * (derivative evaluated at current value of function)
- Good for small step sizes, fails for large step sizes
## Explicit Euler [[Stability (Numerical Methods)]]
- For the numerical method to [[Numerical Convergence]], the computed values should not diverge. 
- $(1−ah)$ should not cause $x_n$​ to oscillate wildly or grow exponentially
- Key conditions:
	- $∣1−ah∣<1$
	- $h<\frac{a}{2}$
	- This means that **explicit Euler requires small time steps** for stability when solving stiff equations.​