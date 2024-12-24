up:: [[Banking MOC]]
tags:: #Finance 
# Value at Risk
- A level of loss such that there is a given probability of losing more than that amount
	- tells you the minimum predictable loss
- A subjective model (based on parameter decisions), therefore has model risk

## Model Building Approach
$$VaR = VM \cdot z_{\alpha} \cdot \sigma \cdot \sqrt{N}$$
- VM: market value of portfolio
- z: confidence interval for estimation (1.65 for 95%, 2.33 for 99%) [[Probability MOC]]
	- Depends on risk appetite (higher interval = higher risk)
- σ: Volatility of asset returns
	- Daily volatility = σyearly / √252 
		- 252 trading days per year
	- Monthly = daily VaR * square root of 22
- N: Time horizon (time to liquidate positions)
	- Higher time horizon, more risk appetite
#### Assumptions
- [[Normal Distribution]] (options are non normal and can't use the standard model building approach)
- Linear payoff
- 0 mean
- Constant standard deviation
- Constant correlation
- No serial correlation in risk factors (independent shocks)
### DEAR
$$ \text{DEAR} = VM \cdot \sigma \cdot z_{\alpha} $$
= Market value of position * price sensitivity * potential adverse move
- or
= Market value of position * price volatility
- where price volatility = modified [[Duration Model]] * potential adverse move
	- Modified duration for bonds, market beta for equities

- Daily earnings at risk (VaR standardized to daily)
- N = 1 -> doesn't need to be included 
- Uses a **delta normal approach**

- ***VaR = DEAR * √N***
	- 10 day var: N = 10
### For Portfolios
$$ % Portfolio VaR formula
\text{VaR}_{\alpha} = VM \cdot z_{\alpha} \cdot \sigma_p $$
- Standard deviation is now for the portfolio, measured by:
$$ \sigma_p = \sqrt{\sum_{i=1}^{n} \sum_{j=1}^{n} w_i w_j \sigma_i \sigma_j \rho_{ij}} $$
- **wi​**: Weight of the i-th asset in the portfolio.
- **σi​**: Standard deviation of the i-th asset's returns.
- **ρij​**: Correlation coefficient between the returns of assets i and j.
- **n**: Number of assets in the portfolio
## Historical Simulation Approach
- Main idea: past is the best proxy for the future
- How it works:
	- 1: selecting a sample (ex: 250 daily observations)
	- 2: revaluing position/portfolio
	- 3: reconstructing empirical frequency distribution of portfolio values and their changes
	- 4: cutting the distribution at the percentile corresponding to the desired confidence level (250 observations = 3 worst losses = 1% VaR)
![[Screenshot 2024-05-16 at 9.29.12 AM.png]]
## [[Monte-Carlo Simulation]] Approach
- Used when data is limited
- Estimate parameters (meant, std, etc) using a [[T Distribution]] to reflect the hypothetical historical sample
- Useful for non-linear portfolios ([[Derivatives MOC]])

## Expected Shortfall
- Expected loss given that VaR has been exceeded
	- Weighted average of all losses above VaR
		- sum of all: (*Probability * loss amount)
- Essentially shows the fatness of the tails of the distribution (intensity of black swan events)
## Stressed VaR
- Try to replicate VaR under a situation of distress
