up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# Differencing
- We can difference repeatedly, in fact we can do it $d$ times, **stock returns** in indirectly performs a differencing operation once.  
$$(Price_{t+1}-Price_{t})/Price_{t}$$
- Makes time series [[Stationarity]]
## Proper way to do it
`np.log(price_t) – np.log(price_t-1)`
