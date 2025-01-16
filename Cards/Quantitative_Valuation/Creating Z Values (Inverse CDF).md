up:: [[Quantitative Valuation MOC]]
tags:: #Finance  
# Creating Z Scores
1) Use a random number generator ([[Random Number Generators]]) to generate uniformly distributed random numbers (i.e. range from 0-1)
	- In excel: 
		- `u=rand()` for uniform random numbers
		- `normsinv(u)` to get inverse of normal cdf 
		- **Together = `normsinv(rand())` will make a standard normal number**
1) Map these random numbers to Z scores by computing the inverse [[Cumulative Distribution Function (CDF)]]

## For other distributions
- Normal
	- `normsinv(rand())`
- Chi-squared
	- `chisq.inv(u,1)`