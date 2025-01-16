up:: [[Supervised Learning MOC]]
tags:: #Machine_Learning 
# Filter Methods
### Thresholding Variance 
- drop all features with low variance, as these give little extra directional predictive power
	- Non categorical
		- Use own judgement for a threshold (like 0.5)
	- Binary
		- Use [[Bernoulli Random Variable & Processes]] variance formula
			- P(1-P) becomes threshold, you select P
### Highly Correlated Features
- Look at upper triangle of [[Covariance Matrix]] 
	- Remove highly correlated features 1 by 1
### In [[Classification]]
- Remove categorical features by whichever has the highest [[Chi-squared Distribution]] statistic
- 