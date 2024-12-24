up:: [[Econometrics MOC]]
tags:: #Math
# [[GARCH]] Correction
- Corrects for heteroskedasticity (most of the time) in time series
	- Need to reconfirm with an additonal [[ARCH Test]]
- Uses [[Maximum Likelihood Estimator]]
## Why it corrects
- GARCH basically states that the current conditional variance σt2​ is influenced by a constant α0​, the previous period's squared residual ϵt−1, and the previous period's conditional variance σt−1.
	- Using **lagged conditional variances** to model volatility clustering if there is any *explicitly*
		- Kills heteroskedasticity even if its not there