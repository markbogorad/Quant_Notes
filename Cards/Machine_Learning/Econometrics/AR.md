up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# AR(1)
$$y_t = \phi_0 + \phi_1 y_{t-1} + \phi_2 y_{t-2} + \dots + \phi_p y_{t-p} + \varepsilon_t$$
- Lagged variables being a predictor for the future
- a regression model which depend linearly on the previous terms.
- They try to capture _**momentum** (positive autocorrelation)_ and _**mean reversion** (negative autocorrelation)_ effect from the observed time series.
	- Can correct for [[Serial Correlation]], see [[Correlogram]]
- [[ARIMA]]