up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# Stationarity
## Strong stationary
- A sequence of random variables $Z = {Z_t}_\inf ^ \inf$ is stationary if its **distribution** is invariant to shifting in time
	- All sample moments are the same
	- Intuition
		- If you take any 2 pieces of the time series, these should follow the same distribution
## Weak stationarity
- Mean, variance, and covariance to not vary with time
	- Needs to have mean reversion, constant variance (not a function of time), spread is constant (doesn't become closer with time)
- A sequence of random variables $Z = {Z_t}_\inf ^ \inf$ is weakly stationary if its **first and second moments** are invariant to shifting in time
	- $E[Z_t]$ is independent of t
	- $E[Z_tZ_{t-j}]$ = $f(j)$ for some function of f
		- where $E[Z_tZ_{t-j}]$  us the [[Covariance]] of the [[Stochastic Process]] 
		- $f(j)$ is the correlation of $Z_t$ and $Z_{t - j}$ depends only on the lag of j
			- time independent
- [[ARIMA]] is weakly stationary
## Unit Circle Definition
- An [[ARIMA]] process is stationary if the roots of the characteristic polynomial $P(z)$ are outside of the unit circle 