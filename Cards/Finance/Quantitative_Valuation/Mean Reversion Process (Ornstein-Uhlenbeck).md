up:: [[Quantitative Valuation MOC]]
tags:: #Finance  
# Mean Reverting Process
$$S_{t+1} = S_t + \kappa (\mu - S_t)+\sigma z_{t+1}$$
- $k$ is speed of mean reversion
- $\mu$ is mean
- Index decays exponentially to a long run mean level
- Interest rates, cash flows linked to [[Commodities MOC]], [[FX MOC]]

![[Pasted image 20241112163521.png]]

## Moments
- The variance behaves by hitting a maximum at $\frac{\sigma^2}{(k(2-k))}$
- Mean: $\mathbb{E}[S_{t+j} | S_t] = \mu + (S_t - \mu)(1 - \kappa)^j$
- Variance: $\text{Var}[S_{t+j} | S_t] = \sigma^2 \left( \frac{1 - (1 - \kappa)^{2j}}{\kappa(2 - \kappa)} \right)$
- Covariance: $\text{Cov}[S_{t+j}, S_{t+m} | S_t] = \sigma^2 \left( \frac{1 - (1 - \kappa)^{2j}}{\kappa(2 - \kappa)} \right) (1 - \kappa)^{m - j}$
## Cholesky Decomp
![[Pasted image 20241113173514.png]]

## Use cases
- Modeling oil, interest rates

## Testing for Mean Reversion
- Regress and look at slope coefficient 
- ![[Pasted image 20241113175014.png]]
	- Speed of mean reversion here is 1.44% and the long run mean is $0.7065/0.1441 = 49$
	- 