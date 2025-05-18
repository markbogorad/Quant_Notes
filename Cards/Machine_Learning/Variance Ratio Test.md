up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# Variance Ratio Test
- Test on whether the variance is growing linearly with time, the 2nd moment of the conditions for weak form [[Stationarity]] and like a secondary test to the [[Augmented Dickey Fuller Test]]
$$VR(k) = \frac{\text{Var}(X_{t+k} - X_t)}{k \cdot \text{Var}(X_{t+1} - X_t)}$$
$$Z_{VR} = \frac{VR(k) - 1}{\sigma_{VR}}$$
where
- $( \text{Var}(X_{t+k} - X_t) )$: Variance of $( k )$-period returns.
- $( \text{Var}(X_{t+1} - X_t) )$: Variance of 1-period returns. 
- $( \sigma_{VR} )$: Standard error of the variance ratio under the null hypothesis.

- If $Z_{VR} >$  critical value, then we can reject the null and it's not a random walk