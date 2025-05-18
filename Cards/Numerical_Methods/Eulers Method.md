up:: [[Numerical Methods MOC]]
tags:: #Math
# Eulers Method
- Essentially evaluating a derivative if you don't take the limit
- Current location $(x(t))$ + direction and magnitude of time step $(f(x(t),(t)h))+o(h)$
	- Do this recursively
- Solves first order [[ODE]]s
- [[Explicit Euler]]
- [[Implicit Euler]]
## Derivation
- A derivative is defined as:
$$\frac{dx(t)}{dt} = \lim_{h \to 0} \frac{x(t + h) - x(t)}{h}$$
- Using a small step size $( h )$, we approximate:
$$x(t + h) = x(t) + f(x(t), t) h + o(h)$$
- Here:
	- $( f(x(t), t) )$ represents the rate of change at $( x(t) )$.
	- $( o(h) )$ denotes higher-order terms (which are small for small $( h )$).

The iterative formula for Euler's method becomes:
$$x_{n+1} = x_n + h f(x_n, t_n)$$
Where:
- \( x_n \) is the value at step \( n \),
- \( t_n \) is the time at step \( n \),
- \( h \) is the step size.
## Extension to [[SDE]]
- The discrete approximation for the SDE is:
$$x_{n+1} - x_n \approx f(x_n, t_n) \, h + g(x_n, t_n) \, h^{1/2} N$$
Where:
- $( h )$: The time step size.
- $( N )$: A standard normal random variable $(( N \sim \mathcal{N}(0, 1) ))$ representing stochastic noise.
