up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# GARCH
- GARCH(p, q): There are further developments like GARCH(p, q) which is an [[ARIMA]] model further applied to model the variance of a time series.
	- Essentially [[ARIMA]] applied to the [[Residuals]]
- G/ARCH should only ever be applied to series that do not have any trends or seasonal effects, i.e. that has no (evident) serially correlation.
- GARCH regresses against past squared errors and past squared variance.
- Volatility Clustering --> volatility bundling together during certain time periods (like a trend in volatility)
	- GARCH is essentially ARMA for volatility
		- GARCH MA component --> squared error of variance
	
- GARCH(p, q) is like an ARMA model, but applied to the variance of a time series i.e., it has an autoregressive term and a moving average term for variance.
$${Var}(\epsilon_t) = \alpha_0 + \beta_1 {Var}(\epsilon_{t-1})+ \alpha_1 \epsilon_{t-1}^2 +w_t$$
## Combined ARIMA and GARCH
When combined in an ARIMA-GARCH model:

1. Mean Prediction: The ARIMA part models and forecasts the expected value of the time series at each point.
2. Variance Prediction: The GARCH part models and forecasts the variance around that expected value.
3. Comprehensive Forecasting: Together, they provide a forecast that includes both the expected value (from ARIMA) and a measure of uncertainty around that value (from GARCH).