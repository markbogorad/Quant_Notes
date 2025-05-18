up:: [[Numerical Methods MOC]]
tags:: #Math 
# Boundary Conditions
- Boundary conditions are constraints imposed on the solutions of differential equations to ensure uniqueness and well-posedness
- In [[ODE]]
	- Boundary conditions are usually given at specific points of the independent variable - necessary to uniquely determine a solution.
	- **Initial Condition (IC)**: AKA initial value problem - specifies the value of the function at a starting point.
		- Solution to the PDE at any time = 0, and the equation evolves from this seed
	- **Boundary Condition (BC)**: AKA boundary value problem - specifies function values or derivatives at two or more points.
- In [[PDE]]
	- For **PDEs**, boundary conditions are imposed over a region (domain) and can be classified as:
		- Elliptic (B² - 4AC < 0): Steady-state solutions (e.g., Laplace’s equation). No time dependence.
		- Hyperbolic (B² - 4AC > 0): Wave-like solutions (e.g., wave equation).
		- **Parabolic (B² - 4AC = 0)**: Diffusion-like processes (e.g., heat equation or Black-Scholes equation).
	- Think of it as examining the whole x-axis
- [[Black-Scholes]]
	- In American options, there is a free boundary problem - finding the boundary is part of the problem
		- Boundary is optimal exercise