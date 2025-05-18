up:: [[Numerical Methods MOC]]
tags:: #Math 
# Lipschitz Condition 
$$\| f(y, t) - f(x, t) \| \leq L \| y - x \|$$ Where: 
- $( f(y, t) )$ and $( f(x, t) )$ are the function values at two different points $(y)$ and $(x)$ for the same $(t)$, 
- $( L )$ is the Lipschitz constant, 
- $( \| \cdot \| )$ represents the norm (e.g., absolute value in 1D).

### Key Properties of the Lipschitz Condition
1. Ensures **existence** of a solution. 
2. Guarantees **uniqueness** of the solution. 
3. Implies \( f(x, t) \) is **continuous**, but not all continuous functions satisfy the Lipschitz condition.  
### Practical Example of Failure 
- Consider the ODE: 
- $\frac{dx}{dt} = x^2 - ( f(x, t) = x^2)$ is continuous but not Lipschitz because its derivative grows unbounded as \(x\) increases. 
- For initial conditions near $(x_0 = 0)$, the solution is unique. 
- For larger $(x_0)$, uniqueness may fail due to the rapid growth of $(x^2)$. 
### Example of Non-Unique Solutions 
- Consider: $\frac{dx}{dt} = \sqrt{x}$, $\quad x(0) = 0$ This has multiple solutions because $( f(x, t) = \sqrt{x})$ is not Lipschitz near $( x = 0 )$.`

