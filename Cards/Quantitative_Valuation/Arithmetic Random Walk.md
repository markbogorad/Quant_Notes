up:: [[Probability MOC]], [[Stochastic Process]], [[Quantitative Valuation MOC]]
tags:: #Math #Finance  
# Arithmetic Random Walk
$$S_{t+1} - S_t = \mu + \sigma z_{t+1}$$
$$\text{1 Step Fcast : }S_{t+j} = S_t + j \mu + \sigma \sum_{i=1}^j z_{t+i}$$
- A random process that grows linearly with time
- Standard deviation increases indefinitely with the square root of time -> stochastic process becomes more uncertain as we go further into the future
- Mean
	- $\mathbb{E}[S_{t+j} | S_t] = S_t + j \mu$
- Variance
	- $\text{Var}[S_{t+j} | S_t] = j \sigma^2$
	
>  we may also think of $S_t$ as a vector of jointly normally distributed variables. That is, we could generate random outcomes for the vector by taking a dataset of independent standard normally distributed numbers and multiplying by the transpose of the [[Cholesky Decomposition]] of this covariance matrix.

## Limitations
- Process becomes negative -> not realistic for stocks
## Use Cases
- Estimating a company's cash flows
- Modeling differences between prices

