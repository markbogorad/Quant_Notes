up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# MA
$$y_t = \mu + \varepsilon_t + \theta_1 \varepsilon_{t-1} + \theta_2 \varepsilon_{t-2} + \dots + \theta_q \varepsilon_{t-q}$$
- Current value of a time series is influenced by past random shocks (errors)
	- Think if the MA factor as previous uncertainties playing a role in prediction
	- Think of these shocks as arising from financial news like earnings surprises or interest rate adjustments.
- Using errors (residuals) as features in the model, this cancels out the effect of the errors because you are regressing against the historical residuals. MA(5) = 5 lagged residuals
- Can model some of the fat-tailed nature of stock returns.


