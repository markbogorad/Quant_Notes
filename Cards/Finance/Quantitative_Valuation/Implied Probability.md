up:: [[Quantitative Valuation MOC]]
tags:: #Finance  
# Implied Probability
- Derives the [[Probability Density Function (PDF)]] of [[Option Intro]] using [[Implied Volatility]]
- By analyzing [[The Volatility Smile]], we can estimate where the option will move in the future
	- By taking the **first and second derivatives** of the option price with respect to **the strike price** (using some calculus tricks), we can estimate the "implied probability" of the asset hitting certain prices in the future. Essentially, these derivatives help us "extract" the probability that the market is assigning to different price levels.
		- Not delta and gamma, this is with respect to strike!
- The Shimko method smoothes the implied volatility so you can take the derivative of the function
## The Process
1) Obtain volatility smile
2) estimate the implied probability of the option hitting certain prices in the future by analyzing the 1st and 2nd derivative of the option price with respect to strike
3) Can smooth implied volatility using the Shimko method (1993)
	- 