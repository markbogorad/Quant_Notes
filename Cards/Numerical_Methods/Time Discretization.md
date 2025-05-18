up:: [[Numerical Methods MOC]]
tags:: #Math 
# Time Discretization
- Breaking down a continuous time variable into discrete steps
	- Ex: breaking down [[Black-Scholes]] so it can be solved with something like [[Crank Nicholson]]
	- Done so computers can work on these equations -> can't operate in continuous time
- This is basically what happens in [[Finite Difference Methods]] - we replace the derivative with a finite difference approximation
## Issues with Time Discretization
- Approximation error - FDM might deviate from true value, potential causing a lack of [[Numerical Convergence]]
- Computationally expensive for small time steps
- Errors might grow uncontrollably - no[[Stability (Numerical Methods)]]
- Hard to implement [[Boundary Conditions for PDEs]]
### Unevenly Spaced Discretization (Non-Uniform)
- the time steps $Δt$ are not constant across the time grid. 
- Instead of dividing time into uniform intervals, you use [[Runge Kutta Adaptive Step Size]]
- Ex: [[American Option Numerical Methods]]
	- **Small time steps** near expiration to capture rapid changes in the early-exercise boundary.
	- **Larger time steps** farther from expiration, where changes are slower.