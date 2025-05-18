up:: [[Numerical Methods MOC]]
tags:: #Math 
# FULLY IMPLICIT Forward Time Centered Space FDM
$$\frac{u_i^{n+1} - u_i^n}{\Delta t} = \alpha \frac{u_{i+1}^{n+1} - 2u_i^{n+1} + u_{i-1}^{n+1}}{(\Delta x)^2}$$
- Rearrange the equation into a linear system $A⋅Un+1=b$
- Solve the system at each time step to get $u_i^{n+1}$​ for all grid points.
