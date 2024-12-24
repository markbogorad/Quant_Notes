up:: [[Probability MOC]], [[Stochastic Process]], [[Quantitative Valuation MOC]]
tags:: #Math #Finance  
# Geometric Random Walk
$$S_{t+j} = S_t \exp \left[ \left( \alpha - \frac{\sigma^2}{2} \right) j + z \sigma \sqrt{j} \right]
$$
- A random process that evolves exponentially
- AKA [[Geometric Brownian Motion]] for continuous time
- /2 term -> corrects for an overestimation of volatility so it grows at the proper mix of $\alpha$ (expected return) and $\sigma$
## Use cases
- Discrete time security values modeling
	- Basis of the [[Black-Scholes]] merton model
	- Issue: securities are actually leptokurtic but GRW doesn't capture this (negative skew)