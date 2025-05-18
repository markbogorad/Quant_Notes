up:: [[Numerical Methods MOC]]
tags:: #Math
# Implicit Euler
- Unlike the [[Explicit Euler]], where the next step is computed using **known values** at the current time step, the implicit Euler method involves solving an equation implicitly **at the new time step.**
$$x_{n+1} = x_n + h f(x_{n+1}, t_{n+1})$$
- h (step size) is small but not 0
- Key difference is $t_{n+1}$
- The function $f(x_{n+1}​,t_{n+1}​)$ depends on $x_{n+1}$​, which means we cannot directly compute $x_{n+1}$​.
- Instead, we have to **solve an equation** to find $x_{n+1}​, usually via numerical root-finding methods [[Newtons Method]]
### Stability
- **Unconditionally stable**
- Condition on step size h
- If coefficient a is reasonably big, h has to be small for convergence