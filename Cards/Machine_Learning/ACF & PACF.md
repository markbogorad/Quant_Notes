up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# ACF
- Linear correlation between a time series and it's lagged values
- Used for identifying [[MA]] order
- Outside of shaded region = significant
- Inside region = insignificant
# PACF
- Looks at the direct effect of lagged valued (not cumulative, intermediate lag effects)
- which length of a lookback window has informative data
	- How many lags have informative correlations
	- Outside of the shaded region (5% confidence interval for ljung box) is a non significant correlation
- Used for identifying [[AR]] order


![[Screenshot 2024-12-31 at 10.18.53 AM.png]]