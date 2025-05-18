up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# Smooth Transition Autoregressive Model
$$y_t = \phi_0 + \phi_1 y_{t-1} + \dots + \phi_p y_{t-p} + G(z_t; \gamma, c) (\psi_0 + \psi_1 y_{t-1} + \dots + \psi_p y_{t-p}) + \varepsilon_t$$
- [[Threshold Autoregressive (TAR)]] family
- The STAR model assumes a smooth transition between regimes rather than abrupt switches. 
- The degree of transition is governed by a [[Logistic Regression]] or exponential function, allowing for gradual changes in the dynamics of the system.