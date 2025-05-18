up:: [[Oil Markets MOC]]
tags:: #Finance 
# WTI - Brent Accordion
- Strategy: front run the behavior of the physical [[Locational Spread]] traders without owning a ship with [[Energy Statistical Arbitrage]]
	- We know they're going to be selling Brent and buying WTI when the 2 diverge by more than cost of shipping
- WTI is more popular
	- Often used as a hedging tool and allows for physical delivery in Cushing Oklahoma
- Brent
	- Waterborne -> barrels easily shipped anywhere
	- Based on a basket of nordic crude oils
	- Brent trading is more focused on locational factors, as their business is closer related to shipment logistics
	- Brent is implicitly also dependent on freight futures, adding a variable to the equation
## Accordion
- Since 2015, the WTI and Brent spread has been in accordion due to lifting of geopolitical frictions
## The Strategy
- [[Energy Statistical Arbitrage]]
$$\begin{equation} \pi_V(S_t) = \begin{cases} -1, & \text{if } S_t - MA_t(S_t; n) > \varepsilon, \\ +1, & \text{if } S_t - MA_t(S_t; n) < -\varepsilon, \\ 0, & \text{if } |S_t - MA_t(S_t; n)| \leq \varepsilon. \end{cases} \end{equation}$$
- Taking advantage of large deviations from the WTI-Brent spread
- [[MA]] is there to approximate equilibrium level of spread, which the threshold will be on
	- Implicitly betting on some [[Mean Reversion Process (Ornstein-Uhlenbeck)]]
- n is the lookback period
- Sharpe of 1.0 since 2015
### Important time mismatch
- You need t-1 futures contract in buying country and T in selling country because shipping takes 1 month
- Buy F1 WTI -> ship -> Sell F2 Brent