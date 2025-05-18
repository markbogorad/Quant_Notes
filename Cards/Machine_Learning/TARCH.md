up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# TARCH (Threshold GARCH)
$$h_t = \omega + \alpha_1 \varepsilon_{t-1}^2 + \gamma_1 \varepsilon_{t-1}^2 I(\varepsilon_{t-1} < 0) + \beta_1 h_{t-1}$$
- Captures asymmetry in volatility -> positive and negative shocks to have different effects on volatility. 
- It captures the "leverage effect," where negative shocks typically lead to higher volatility than positive shocks of the same magnitude.