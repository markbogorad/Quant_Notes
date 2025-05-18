up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# ADF Test
- A test on mean reversion
$$\Delta Y_t = \alpha + \beta t + \gamma Y_{t-1} + \sum_{i=1}^p \phi_i \Delta Y_{t-i} + \varepsilon_t$$
where:
- $( \Delta Y_t = Y_t - Y_{t-1} ):$ the first difference of $( Y_t )$ 
- $( \alpha )$: Intercept (drift term) 
- $( \beta t )$: Time trend (optional, included if the series has a deterministic trend)
- $( \gamma )$: Coefficient of $( Y_{t-1} )$, which is the focus of the test
	- If gamma is anything but 0, it is not a [[Random Walks in Time Series]]
- Null hypothesis $(( H_0 ))$: $( \gamma = 0 )$ (unit root exists, non-stationary) 
- Alternative hypothesis $(( H_1 ))$: $( \gamma < 0 )$ (stationary) 
- $( \sum_{i=1}^p \phi_i \Delta Y_{t-i})$: Lagged differences of $( Y_t )$, included to account for autocorrelation in residuals. $( \varepsilon_t )$: Error term (white noise).
## Test Statistic
$$\tau = \frac{\hat{\gamma}}{\text{SE}(\hat{\gamma})}$$
- $( \hat{\gamma} )$: The estimated coefficient of $( Y_{t-1} )$ from the regression equation. 
- $( \text{SE}(\hat{\gamma}) )$: The standard error of $( \hat{\gamma} )$.