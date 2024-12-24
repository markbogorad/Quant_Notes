up:: [[Econometrics MOC]]
tags:: #Math
# White Test
- For cross sectional [[Heteroskedasticity]] and general time series heteroskedasticity
- **Null:** homoskedasticity (want high p values so you can't reject)
- **Alternative:** heteroskedasticity 
- Identifies the presence of heteroskedasticity when it's driven by 1 variable, its square, or its product in the regressor
	- Basically sees if 1 regressor drives the heteroskedasticity

**How it works:**
- Runs the original regression
- Use residuals to create an auxiliary regression and squared residuals are regressed onto the original independent variables, their squares, and their sums
	- Residuals are Y here
- Compute test statistic and degrees of freedom
## Test Statistic
$$ W = NR^2 \sim \chi^2(m)$$
- Total observations * [[R Squared]] of auxiliary regression
- N: observations
- Distributed as a [[Chi-squared Distribution]] with M degrees of freedom
- M: the amount of regressors excluding constant (also degrees of freedom)

## If detected
- Try to correct with [[Huber-White Test]] (will show presence of White's Heteroskedasticity)
