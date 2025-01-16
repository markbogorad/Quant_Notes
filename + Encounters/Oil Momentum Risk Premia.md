up:: [[Oil Markets MOC]]
tags:: #Finance 
# Momentum
- [[Algorithmic Trading in Oil]]
- Oil momentum has it's roots in [[Dynamic Theory of Storage]]
	- These trading strategies usually look for imbalances in inventory supply and demand
	- Largely dependent to parameter selection and prone to overfitting
## Fundamentals
- Oil supply and demand are price inelastic - slow to adjust to changes
- Status quo is naturally more likely to prevail tomorrow
- Oil consumption follows rigid business cycles, oil inventories are therefore persistent and so are prices
#### Time series trend following vs cross sectional momentum
- [[Time Series MOC]]
- Time series: generate signals based on assets own price history
- cross sectional: used in conjunction with larger commodity portfolios where you buy highest momentum and sell lowest momentum ranks with neutral overall exposure
	- Cross sectional is cross asset here
## Time Series Momentum
$$M_t(P_t;n)=P_t-MA_t(P_t;n)$$
- Momentum = spread between latest price and moving average ([[MA]])
#### Ex: 5 day momentum
$$\begin{equation} \sum_{i=1}^{n-1} \left( \frac{n - i}{n} \right) dP_{t-i+1} \end{equation}$$
- Basically weighted sum of price changes, with weights decreasing as you go further into time
## Momentum Signal
- If spread is $\geq$ 0, buy
- If spread is < 0, short

## Backtests
- Mid strategy
- 10% return
- 0.27 [[Information Ratio]] (bad)
- Max drawdown 25% (bad)
- Momentum trading strats are prone to overfitting, so they look better than they are

## Useful alternative: smoothed signal sensitivity (MA crossover)
- A lot of momentum strategies are overparameterized
- Momentum definition adjusted to the difference between MAs, i.e. an MA crossover
$$M_t(m,n)=MA_t(m)-MA_t(n),m<n$$
- Largest weights closer to the start of the lookback window
## Alternatives
- There are many parameters you can add and thresholds to overlay on top of traditional momentum strategies
	- Bottom line is they underperform and result in random stuff
	- Useful to include with other trades