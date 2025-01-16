up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# Standard Error
- Standard error of an estimator
**General Formula:**
$$ s = \sqrt{\frac{\sum u_{i}^{2}}{n - k}} $$
- Where
		- n is number of observations
		- K is number of regressors 
- Standard errors are a measure of the precision of the beta hat estimates (how reliable the [[Point Estimators]] is)
- Equivalent to the square root of the estimated variance of the estimator
- The larger the standard error, the more noisy are the estimates
	- As a rule of thumb, *standard error should be less than half the value of it's estimated coefficient*
		- If so, estimator is precise

**For standard error of a specific coefficient:** this is more common!
- Same formula for standard deviation of the sample mean
- Square root of the estimated variance of the errors (sigma squared)
$$ \text{se}(a) = s \sqrt{\frac{1}{N \sum_{i} (x_{i} - \overline{x})^{2}}} $$

- where
	- S = standard error general formula
		- The bigger the S, the bigger the standard error
	- Denominator = sample variance of X
	- N = sample size
- In EViews, "SE of Regression"