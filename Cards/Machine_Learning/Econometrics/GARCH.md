up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# GARCH
$$h_t = \omega + \alpha_1 \varepsilon_{t-1}^2 + \beta_1 h_{t-1}$$
- Past volatility (squared variance) + past shocks
	- Similar structure to [[AR]] + [[MA]] for [[ARIMA]]
	- Essentially [[ARIMA]] applied to the [[Residuals]]
- G/ARCH should only ever be applied to series that do not have any trends or seasonal effects, i.e. that has no (evident) [[Serial Correlation]]
- Volatility Clustering --> volatility bundling together during certain time periods (like a trend in volatility)
	- GARCH is essentially ARMA for volatility
		- GARCH MA component --> squared error of variance
	
- GARCH(p, q) is like an ARMA model, but applied to the variance of a time series i.e., it has an autoregressive term and a moving average term for variance.
$${Var}(\epsilon_t) = \alpha_0 + \beta_1 {Var}(\epsilon_{t-1})+ \alpha_1 \epsilon_{t-1}^2 +w_t$$
## GARCH Family Extension
- [[TARCH]]
- [[FIGARCH]]
- [[EGARCH]]