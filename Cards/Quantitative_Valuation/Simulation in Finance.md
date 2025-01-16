up:: [[Quantitative Valuation MOC]]
tags:: #Finance  
# Simulation
- Typically the least accurate, but most flexible method
- Put simply, we generate a large sample of possible outcomes and estimate the result of the model using the average
## The Process
 - Collect a lot of data (N) of random numbers $z$
- Compute Z scores f(z) as a function of random numbers (outcomes)
	- Compute average ($\bar{X}$) of f(z), this is your [[Expectation]] estimate
	- Compute standard deviation of f(z)
	- Compute standard error -> standard deviation / $\sqrt{N}$
	- Compute maximum likely error -> m * (standard error), where m is your selection (m=2 usually)
	- Solution $= E[f(z)] = \bar{X} \pm ms/\sqrt{N}$
  - You can use **any distribution** by taking the inverse of it's [[Cumulative Distribution Function (CDF)]]