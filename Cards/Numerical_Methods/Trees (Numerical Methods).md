up:: [[Numerical Methods MOC]]
tags:: #Math 
# Trees
- Discrete time models
- Deals with path dependency and exploits boundary conditions
- 2 trees with different volatilities can solve for [[Vega]]
## Binomial Tree
- This is [[Cox, Ross, Rubenstein (CRR)]]
$$u = e^{\sigma \sqrt{\Delta t}}, \quad d = e^{-\sigma \sqrt{\Delta t}}$$
$$V = e^{-r \Delta t} \left( p V_u + (1-p) V_d \right)$$
$$p = \frac{e^{r \Delta t} - d}{u - d}$$
$$S_n = S_0 u^j d^{n-j}$$
## Trinomial Trees
- Include a probability of stsaying at the same level
$$p_u = \frac{1}{2} \left( \frac{\sigma^2 \Delta t}{(\Delta x)^2} + \frac{\mu \Delta t}{\Delta x} \right), \quad
p_m = 1 - \frac{\sigma^2 \Delta t}{(\Delta x)^2}, \quad
p_d = \frac{1}{2} \left( \frac{\sigma^2 \Delta t}{(\Delta x)^2} - \frac{\mu \Delta t}{\Delta x} \right)
$$