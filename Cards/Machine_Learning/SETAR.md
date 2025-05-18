up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# SETAR Model
$$y_t =
\begin{cases}
\phi_{11} y_{t-1} + \dots + \phi_{1p} y_{t-p} + \varepsilon_t & \text{if } y_{t-d} \leq \tau \\
\phi_{21} y_{t-1} + \dots + \phi_{2p} y_{t-p} + \varepsilon_t & \text{if } y_{t-d} > \tau
\end{cases}$$
- The SETAR model extends the [[Threshold Autoregressive (TAR)]] model by allowing each regime to have its own [[AR]] structure. 
- It is particularly useful for modeling time series with nonlinear patterns and regime switches that are determined by the data itself.