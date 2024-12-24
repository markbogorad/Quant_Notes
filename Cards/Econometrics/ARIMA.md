up:: [[Econometrics MOC]]
tags:: #Math
# ARIMA Models
- Both the [[AR]] and [[MA]] components simultaneously
- Still a linear model
- Forecasts are not made by first calculating the AR component and then applying the MA component or vice versa. Instead, the ARMA model combines these components into a single equation.
$$x_{t}=\alpha_{1} x_{t-1}+\ldots+\alpha_{p} x_{t-p}+w_{t}+\beta_{1} w_{t-1}+\ldots+\beta_{q} w_{t-q}$$
The **ARIMA** (_**p, d, q**_) model - Autoregressive Integrated Moving Average Models - is a natural extension of the **ARMA**model and essentially performs **differencing** to make a time series more stationary.

- The parameter _**p**_ is the number of autoregressive terms or the number of “lag observations.” It is also called the “lag order,” and it determines the outcome of the model by providing lagged data points.
- The parameter _**d**_ is known as the degree of differencing; it indicates the number of times the lagged indicators have been subtracted to make the data stationary.
- The parameter _**q**_ is the number of forecast errors in the model and is also referred to as the size of the moving average window.