up:: [[Econometrics MOC]]
tags:: #Math #Finance  
# MA
- Think if the MA factor as previous uncertainties playing a role in prediction
- MA(q) are also a regression model and are closely related with Autoregressive models, but they are instead **a linear combination of past error terms w**, as opposed to a linear combination of past observations x.
$$x_{t}=w_{t}+\beta_{1} w_{t-1}+\ldots+\beta_{q} w_{t-q} = \sum_{i=1}^{q} \beta_{i} w_{t-i}+w_{t}$$
The motivation for the MA model is that we can explain "shocks" in the error process directly by fitting a model to the error terms, where $w_t$ is the white noise term.

- Think of these shocks as arising from financial news like earnings surprises or interest rate adjustments.
- They could help us model the effect these shocks have on the future stock returns by modelling changes in autocorrelation.
- Considering that it models on past errors, it can accommodate non-Gaussian distributions and model some of the fat-tailed nature of stock returns.
- It is not able to model heteroskedasticity and skew distributions, for that other innovations is needed.
- Again: the purpose of our modelling is to eventually find a model for our time series where the **residuals** are **white noise**.


> Using errors (residuals) as features in the model, this cancels out the effect of the errors because you are regressing against the historical residuals. MA(5) = 5 lagged residuals