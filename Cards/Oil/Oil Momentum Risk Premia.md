up:: [[Oil Markets MOC]]
tags:: #Finance 
# Momentum
- [[Algorithmic Trading in Oil]]
- Oil momentum has it's roots in [[Fundamental Oil Theory]] and [[Oil Inventories]]
	- These trading strategies usually look for imbalances in inventory supply and demand
	- Largely dependent to parameter selection and prone to overfitting
- **Essentially trend following**
- Works particularly well during crises - will make a lot of money on the fast way down shorting
	- Hedge funds are marketing this like a put option - replicating a put by trading very fast
## Fundamentals
- Oil supply and demand are price inelastic - slow to adjust to changes
	- If supply exceeds demand today, it's most likely giving t be the same tomorrow - inventories will be increasing and via theory of storage you translate this into an increase in prices
- Status quo is naturally more likely to prevail tomorrow
- Oil consumption follows rigid business cycles, oil inventories are therefore persistent and so are prices
#### Time series trend following vs cross sectional momentum
- [[Time Series MOC]]
- Time series: generate signals based on assets own price history
- cross sectional: used in conjunction with larger commodity portfolios where you buy highest momentum and sell lowest momentum ranks with neutral overall exposure
	- Cross sectional is cross asset here
## Time Series Momentum
$$M_t(P_t;n)=P_t-MA_t(P_t;n)$$
- Momentum = spread between todays price and moving average ([[MA]])
- If spread is $\geq$ 0, buy
- If spread is < 0, short
#### Academic Definition of Momentum
- Write the definition in terms of returns (price changes) instead of pure price
$$\begin{equation} \sum_{i=1}^{n-1} \left( \frac{n - i}{n} \right) dP_{t-i+1} \end{equation}$$
- The weights become monotonically decreasing in this example
	- The academic and practitioner definitions match as long as weights are linearly decreasing
## Backtests
- Mid strategy
- 10% return
- 0.27 [[Information Ratio]] (bad)
- Max drawdown 25% (bad)
- Momentum trading strats are prone to overfitting, so they look better than they are

## Useful alternative: smoothed signal sensitivity (MA crossover)
- A lot of momentum strategies are overparameterized
	- This essentially gives confirmation instead of trading on a single day change because you're looking at the averages between 2 periods
$$M_t(m,n)=MA_t(m)-MA_t(n),m<n$$
- The weights here are no longer linearly decreasing
- Instead, **weights increase up to the length of the shorter term moving average**, then decrease linearly
![[Pasted image 20250216114701.png]]
- Left graph - weights peak at shorter MA(m)
- Right graph - strategy is very prone to overfitting (random-ish selections do well because they happen to fall on days where there were favorable moves). Better to choose the most stable parameters instead of best performing 
## Additional variations
- Combining frequencies - aggregate signal as weighted average of several signals
	- Short term: daily vs weekly
	- Medium term: weekly vs monthly
	- Long term: monthly vs yearly
- Threshold momentum
	- Add a parameter epsilon to basically ensure your momentum is strong
- Time follow through
	- Require momentum to hold for a certain period before trading
- Follow Smart Money
	- This strategy is momentum, but specifically for order flow of NCs (non commercial traders), who are smart money