up:: [[Risk Management MOC]]
tags:: #Finance 
# Historical Simulation VaR
- VaR derived from historical PnL distribution - looking at the literal n-th worst outcome
	- 1% VaR - 2 times per year event, 5% VaR - a monthyl occurance
- Issue: portfolio today is not representative of the past
	- One possible solution: **Calibrating** by fit a Taylor series onto it capturing as many sensitivities as possible (Delta, Gamma, Cross Gamma)
		- The more you include, the more accurate
## Pros
- Simple
- Non parametric
- Easier to aggregate
- Intuitive
## Cons
- Need a lot of historical data 
	- Can have bad data
- Hard to use for new products
- Difficult for non-linear portfolios
## Steps for historical sim
1. Collect position data
2. Bucket to observable risk indices
3. Calculate sensitivities (first, second: deltas, gammas
4. Calculate returns of indices
5. "Shock" portfolio with returns data
6. Calculate hypothetical P&L figures
7. Rank P&L figures and get order statistic