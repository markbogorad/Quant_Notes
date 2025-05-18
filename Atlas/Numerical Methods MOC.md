up:: [[Home]]
tags:: #MOC 
# Numerical Methods
## Fundamental Concepts
- [[Numerical Convergence]]
- [[Consistency (Numerical Methods)]]
- [[Stability (Numerical Methods)]]
	- [[Von Neumann Stability]]
- [[Explicit vs Implicit Methods]]
- [[Superposition]]
- [[Time Discretization]]
## 1-Dimensional Root Finding
- [[Root Finding (Numerical Methods)]]
- [[Bisection Method]]
- [[Secant Method]]
- [[Newtons Method]]
	- [[Newton-Raphson Root Search]]
- [[Brent Method]]
## Solving ODEs
- [[ODE]]
	- [[Picard Existence Theorem]]
		- [[Lipschitz Condition]]
- [[Eulers Method]]
	- [[Explicit Euler Method]]
	- [[Implicit Euler Method]]
	- [[Milstein Scheme]]
- [[Runge Kutta Methods]]
	- [[2nd Order Runge-Kutta (Midpoint Method)]]
	- [[4th Order Runge-Kutta (RK4)]]
	- [[Runge Kutta Adaptive Step Size]]
- [[Multi-Step Methods]]
	- [[Adams-Bashforth Methods (Explicit)]]
	- [[Adams-Moulton Methods (Implicit)]]
	- [[Dahlquist Equivalence Theorem]]
## Solving PDEs
- [[PDE]]
	- [[Boundary Conditions for PDEs]]
	- [[Linear vs Nonlinear PDE]]
	- [[Black-Scholes]]
	- [[Lax Equivalence Theorem]]
- [[Heat Equation]]
	- [[Separation of Variables (Numerical Methods)]]
	- [[Finite Difference Methods]]
		- [[Explicit FTCS FDM]]
		- [[Fully Implicit FDM]]
		- [[Crank Nicholson]]
- [[Trees (Numerical Methods)]]
	- [[Cox, Ross, Rubenstein (CRR)]]
## Multi Dimensional PDE
- [[Two Dimensional Heat Equation]]
- [[The Curse of Dimensionality]]
- [[Sparse Matrices]]
	- [[Relaxation Methods]]
		- [[Jacobi Method]]
		- [[Gauss Seidel Method]]
		- [[Successive Over-Relaxation]]
- Alternating Direction Methods
## Numerical Integration
- Numerical Integration - trying to approximate a definite integral
- [[Fourier Transforms]] 
	- [[Discrete Fourier Transform]]
	- [[Fast Fourier Transform]]
- [[Monte-Carlo Simulation]]
	- [[Arithmetic Brownian Motion]]
	- [[Geometric Brownian Motion]]
	- [[Mean Reversion Process (Ornstein-Uhlenbeck)]]
- Markov Chain Monte-Carlo
	- Metropolis Monte-Carlo
- Romberg Integration
	- Qtrap Routine
	- Richardson Extrapolation
- Gaussian Quadrature
- Orthanormal Functions
## Random Numbers
quasi random numbers
- [[Transform Methods]]
	- Applied to cumulative monotone distribution functions
		- As long as its monotone increasing, the method works
- [[Rejection Methods]]
- [[Variance Reduction Techniques (Simulation)]]
	- [[Antithetic Sampling]]
	- [[Control Variate Sampling]]
	- [[Stratified Sampling]]
	- [[Importance Sampling]]
		- Take samples of distribution of interest, plug those into the function, take average of those9
- [[Ratio of Uniforms Method]]
- [[Cholesky Decomposition]]
## Interpolation
- Cubic Splines
- Best things to interpolate by: rates, discount factor, log discount factor
## Optimization
## Applications
- [[American Option Numerical Methods]]
	- [[Longstaff Schwartz]]
- [[Hull-White Model]]
- [[Heston Model]]
- [[Vasicek Interest Rate Model]]