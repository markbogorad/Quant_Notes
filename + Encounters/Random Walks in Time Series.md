up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# Random Walks
$$Y_t = Y_{t-1} + \varepsilon_t$$
- $Y_t$ is $Y_{t-1}$ + an error term
- With drift:
	- $Y_t = \alpha + Y_{t-1} + \varepsilon_t$
- Drift and trend:
	- $Y_t = \alpha + Y_{t-1} + \beta t + \varepsilon_t$
## Simple Random Walk Identification
- Do an [[AR]](1) regression and test to see if betas are less than 1. If $\beta=1$ then there is no tendency for mean reversion
	- This is the non augmented version of the [[Augmented Dickey Fuller Test]]
		- Subtract $Y_{t-1}$ from both sides and rename to $\beta_1$ to $\beta_0$
- [[Stationarity]]