up:: [[Probability MOC]], [[Econometrics MOC]]
tags:: #Math
# Adjusted R-Squared
- Similar to [[R Squared]], it is also a measure of variability of data within the model
	- Adjusted r squared adjusts for the number of predictors (regressors k) in the model, useful for analysis when 2 models do not have the same amount of predictors
	- **Key difference:** adjusted r-squared does not increase with additional non-significant variables because it includes K
		- R squared will always = adjusted r squared unless:
			- New predictor improves model more than would be expected or makes the model worse 
	- R squared can be *inflated with useless predictors*, adjusted r squared can't
		- If theres a big difference between the 2, now you know why!
$$ \bar{R}^2 = 1 - \left[ \frac{T - 1}{T - k} (1 - R^2) \right] $$
- T = number of observations
- K = regressors
- R^2 = [[R Squared]]
