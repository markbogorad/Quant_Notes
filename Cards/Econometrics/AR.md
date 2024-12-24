up:: [[Econometrics MOC]]
tags:: #Math #Finance  
# AR(1)
- $AR(p)$ are machine learning models as it is essentially a regression model which depend linearly on the previous terms.
	- Linear generative model 
	- $P^{th}$ order of Markov assumptions (how many steps backward are necessary for prediction)
- They try to capture _**momentum** (positive autocorrelation)_ and _**mean reversion** (negative autocorrelation)_ effect from the observed time series.
$$x_{t}=\alpha_{1} x_{t-1}+\ldots+\alpha_{p} x_{t-p}+w_{t}=\sum_{i=1}^{p}\alpha_{i} x_{t-i}+w_{t}$$
- This is an AR model of order "p", where p represents the number of previous (or lagged) terms/parameters used within the model, $\alpha_i$ is the coefficient, and $w_t$ is a white noise term.
	- wt is white noise
	- Xt is stochastic process
    
- An **AR(p)** model looks at the past **p** values in a time series to make a prediction about the next value. If the recent trend has been upward or downward, the model can predict a continuation of this trend, capturing the idea of momentum. If the series has deviated too far from its average, the model can predict a move back towards that average, capturing the idea of mean reversion.
	- Can correct for [[Serial Correlation]], see [[Correlogram]]
- The purpose of our modelling is to eventually find a model for our time series where the residuals are white noise.