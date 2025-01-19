up:: [[Oil Markets MOC]]
tags:: #Finance 
# Cross-Asset Spread
- Example: [[Oil and OPEC Currencies]]
$$S=CADUSD-\beta \times WTI$$
- Then buy/sell when the pair deviates past a certain band
- Choice of $\beta$ is hard
$$\begin{equation} \pi(S_t) = \begin{cases} -1, & \text{if } S_t - MA_t(S_t; n) > \varepsilon, \\ +1, & \text{if } S_t - MA_t(S_t; n) < -\varepsilon, \\ 0, & \text{if } |S_t - MA_t(S_t; n)| \leq \varepsilon. \end{cases} \end{equation}$$
- There are many good pairs, like in [[Energy Statistical Arbitrage]], these work better in a portfolio:

| **Currency** | **Commodity**           |
| ------------ | ----------------------- |
| CADUSD       | WTI                     |
| NOKUSD       | Brent                   |
| CLPUSD       | Copper                  |
| AUDUSD       | Iron Ore, Coal, LNG     |
| BRLUSD       | Brent, Soybeans, Sugar  |
| RUBUSD       | Brent, Nickel, Platinum |
| ZARUSD       | Platinum, Gold, Coal    |

## Other Commodities
- [[Commodities MOC]]
- Chile is largest copper producer
	- Do CLP/USD to copper, which are highly correlated