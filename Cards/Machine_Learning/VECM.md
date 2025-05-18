up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# Vector Error Correction VECM
$$\Delta y_t = \Pi y_{t-1} + \sum_{i=1}^{k-1} \Gamma_i \Delta y_{t-i} + \varepsilon_t$$
- Long run equilibrium + sum of all [[AR]] components + error
- The VECM is a multivariate model that captures both short-term dynamics and long-term equilibrium relationships among variables. It is used when variables are cointegrated, ensuring that deviations from the long-term equilibrium are corrected over time
- Specifically for [[Cointegration]]
	- $\Pi$ term is the long run equilibrium
- No [[Stationarity]] necessary