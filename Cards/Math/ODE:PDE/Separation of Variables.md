up:: [[Differential Equations MOC]]
tags:: #Math
# Solution by Separation (ODEs)
- For first order [[ODE]] only

1) Rewrite the equation so that the variable and it's differential is on one side
2) Integrate both sides with respect to their variable ([[Integration]])
3) Solve integrals
4) Try to solve for variable of interest
5) If initial conditions give, solve for constant $C$

### Example: Discounted Cashflow

Solve the ODE:

$\frac{dV}{dt} = -rV$


1. $\textbf{Rewrite the Equation:}$

   Separate the variables:

	   $\frac{1}{V} dV = -r dt$

2. $\textbf{Integrate Both Sides:}$

   Integrate both sides:

   $\int \frac{1}{V} dV = \int -r dt$


3. $\textbf{Solve the Integrals:}$

   $\ln |V| = -rt + C$


4. $\textbf{Solve for ( V ):}$

   Exponentiate both sides to solve for $( V )$:
   
   $|V| = e^{-rt + C}$

   Since $( e^C )$ is a constant, we can write it as $( C' )$:
 
   $V = C'e^{-rt}$

   For simplicity, we rename $( C' )$ to $( C )$:

   $V = Ce^{-rt}$


6. $\textbf{Apply Initial Conditions (if given):}$

   If an initial condition such as $( V(0) = F )$ is provided, we can find the constant $( C )$:

   $F = Ce^{-r \cdot 0} = C \implies C = F$

   Therefore, the solution is:

   $V(t) = Fe^{-rt}$


This is the general solution to the differential equation $( \frac{dV}{dt} = -rV )$.


