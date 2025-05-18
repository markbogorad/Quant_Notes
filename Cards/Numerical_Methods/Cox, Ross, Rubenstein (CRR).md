up:: [[Numerical Methods MOC]]
tags:: #Math 
# Cox Ross Rubenstein
- A binomial tree designed to match [[Black-Scholes]]
$$u = e^{\sigma \sqrt{\Delta t}}, \quad d = e^{-\sigma \sqrt{\Delta t}}$$
$$V = e^{-r \Delta t} \left( p V_u + (1-p) V_d \right)$$
$$p = \frac{e^{r \Delta t} - d}{u - d}$$
$$S_n = S_0 u^j d^{n-j}$$

