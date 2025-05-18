up:: [[Numerical Methods MOC]]
tags:: #Math 
# Crank-Nicholson
$$\frac{u_i^{n+1} - u_i^n}{\Delta t} = \frac{\alpha}{2} \left( \frac{u_{i+1}^{n+1} - 2u_i^{n+1} + u_{i-1}^{n+1}}{(\Delta x)^2} + \frac{u_{i+1}^n - 2u_i^n + u_{i-1}^n}{(\Delta x)^2} \right)$$
- The Crank-Nicholson method is a blend of [[Explicit FTCS FDM]] and [[Fully Implicit FDM]]. 
- It uses the **average** of the explicit and implicit methods for the spatial derivative
- It combines the stability of the implicit method with the accuracy of the explicit method.
- Each time step requires solving a linear system, but it’s more accurate than the fully implicit method.

