up:: [[Numerical Methods MOC]]
tags:: #Math 
# Convergence 
- Does the numerical solution approach the exact solution as h→0?
$$\lim_{h \to 0} x_n = x_{exact}(t_n)$$
- Convergence means that as we refine our numerical grid (by taking smaller step sizes h), the numerical solution gets arbitrarily close to the true solution.
- A method must be have both [[Consistency (Numerical Methods)]] and [[Stability (Numerical Methods)]] to be convergent
	- If a method is **consistent** (i.e., small steps closely approximate the true solution) and
	- If the method is **stable** (i.e., errors do not grow uncontrollably),
	- **Then the method is convergent** (i.e., the numerical solution approaches the exact solution as h→0).
- *Errors converge to 0*