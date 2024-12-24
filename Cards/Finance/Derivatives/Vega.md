up:: [[Derivatives MOC]]
tags:: #Finance 
# Vega (aka Zeta aka Kappa)
$$v = \frac{\partial V}{\partial \sigma}$$
- **Sensitivity of option price to volatility ([[Implied Volatility]])**
	- The option value price change per 1-point change in implied volatility.
- Unique: derivative with respect to a parameter (volatility) instead of a variable
	- Parameters may be unstable --> dangerous
	- Ex: [[Black-Scholes]] assumes constant volatility, its actually [[The Volatility Smile]]
- Most used for [[Market Makers]]
- Vega of a portfolio of options = (number of options) x (multiplier) x (option vega)
- [[Call Option]] and [[Put Option]] have the same vegas
- "I'm long 4 vegas" means (vega * qty * multiplier)
## Vega Factors
![[Pasted image 20240629165144.png]]
![[Pasted image 20240629165156.png]]

- 