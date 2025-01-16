up:: [[Quantitative Valuation MOC]]
tags:: #Finance  
# Risk Benchmarks
- Arise when the risk of one investment correlates with another
	- Risks that are uncorrelated from these 2 investments are called residual risks
## Benchmark Risk and Variance Decomposition via Regression
- This is the groundwork to [[CAPM]]
- Risk assuming $r_i$ and $r_m$ are jointly distributed
	- $r_i = a_i+ b_i r_m + \varepsilon$
- Variance of an asset return
	- $\sigma_i^2 = \beta_i^2 * \sigma_m^2 + \sigma_\epsilon^2$
		- e -> error (idiosyncratic risk)
			- No risk compensation to this in Sharpes CAPM (in lintner Capm)
			- Non benchmark (non market) risk
		- m -> market
			- Benchmark risk
## Benchmarking Sharpes (Deriving CAPM)
- Comparing the performance of a stock to its market
- Sharpe of a stock = Sharpe of the market:
	- $\frac{r_i - r}{b_i \sigma_m} = \frac{r_m - r}{\sigma_m}$
- Together, this forms the [[CAPM]]!
	- $r_i = r + b_i (r_m - r)$
	- Which is analagous to the [[General Valuation Equation (GVE)]] definition!
		- $\text{Total expected return} = \text{Time value} (r) + \text{Risk charge} \left[ b_i (r_m - r) \right]$
		- 