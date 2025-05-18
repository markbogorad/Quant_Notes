up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# Chow-Lin Filtering
- A temporal disaggregation technique
	- Data going from lower to higher frequency
## How it works
- Does a linear [[Regression]] -> regress high frequency on lower frequency (high frequency = LF * $\beta$ + error)
- Constraint on lower frequency = sum of all higher frequency brackets
- Error is assumed to be 0 mean stationary

> so basically we go from lower to higher frequency by using OLS regression to sort of interpolate all higher frequency values in between lower frequency values, ensuring we match up via the summation constrain