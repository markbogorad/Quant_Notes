up:: [[Numerical Methods MOC]]
tags:: #Math 
# EXPLICIT Forward Time Centered Space FDM
$$\frac{u_i^{n+1} - u_i^n}{\Delta t} = \alpha \frac{u_{i+1}^n - 2u_i^n + u_{i-1}^n}{(\Delta x)^2}$$
$$u_i^{n+1} = u_i^n + \lambda (u_{i+1}^n - 2u_i^n + u_{i-1}^n)$$
**How it works:**
- Use known values at the current time step ($n$) to compute the value at the next time step ($n+1$).
- March forward in time, updating each grid point.