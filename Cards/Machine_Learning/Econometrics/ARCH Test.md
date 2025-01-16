up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# ARCH Test
- Autoregressive conditional heteroskedasticity
- Test checks if over time the variance is dependent on it's own past
	- If variance at time T depends on a lagged value
	- Aka test for volatility clustering 
- In other words, periods of high volatility tend to be followed by periods of high volatility, and periods of low volatility tend to be followed by periods of low volatility.
- **Null Hypothesis (H0)**: No ARCH effects (i.e., no autoregressive conditional heteroskedasticity). Want high p values
- **Alternative Hypothesis (H1)**: Presence of ARCH effects.

**How it works**
- Runs the original regression (an [[ARIMA]] here probably)
- Use residuals to create an auxiliary regression and squared residuals are regressed onto a constant and q lags of the squared residuals.
- Get test stat, degrees of freedom, and compare critical values
## Correcting
- Use [[Huber-White Test]]
- Use [[GARCH Correction]] (better in this case and for time series)
