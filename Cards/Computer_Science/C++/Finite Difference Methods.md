up:: [[Numerical Methods MOC]],  [[Derivatives MOC]]
tags:: #Math #Finance
# Finite Difference Methods:
- A family of numerical methods that solves [[ODE]] and [[PDE]] by **approximating derivative using nearby points**
	- turning a continuous equation into a discrete problem that computers can solve
		- [[Time Discretization]]
- For example, the first derivative $\frac{dx}{du}$​ can be approximated as:
	- $\frac{du}{dx}≈\frac{u(x+h)−u(x)}{h^2}$ where $h$ is a small time step
- Proxying the derivative by taking the empirical rate of change
## ODE
- [[Explicit Euler]]
- [[Implicit Euler]]
## PDE
- [[Explicit FTCS FDM]]
- [[Fully Implicit FDM]]
- [[Crank Nicholson]]