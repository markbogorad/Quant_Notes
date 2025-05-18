up:: [[Oil Markets MOC]]
tags:: #Finance 
# Vega Trading
- Long term strategy where you fix maturity and trade various trikes along that maturity
- Producer hedging
	- Rich producer - buy put
	- Middle class - buy put, sell call to finance the put (costless collar)
		- Put strike is fixed (bank mandate) but the call strikes are re-purchased daily
	- Poor - 3 way collar (need to leverage)
		- Buy a put spread, sell a call -> hedging by selling volatility (buy 1 option sell 2 -> buy put sell strangle)
			- Cheaper so this allows you to buy a further out of the money call
		- Logic is they only need protection for price increase - if prices decrease they can use real option and shut down production
		- ![[Pasted image 20250303221257.png]]
- Producer hedging options can be mapped to moments
	- ATM straddle = variance
	- Costless collar = skewness
	- Strangle (3 way collar) = kurtosis
- Need a model that prices all of these models consistently
	- Black Scholes doesn't work because you need multiple volatilities
	- Instead, you need a single stochastic process that is consistent with your observable strikes
## Modeling Producer Hedging
- You need unique models to capture the behavior of these collars and 3 way collars
	- Need a stochastic process that is consistent with all 3 strikes
### Dynamic Smile/Skew Delta
- Have a snapshot of the smile - but we need to move the smile through time (during the day as futures move)
	- Skew delta - a correction to Black-Scholes that comes from the smile
- Total dynamic delta:
$$\Delta = \frac{\partial C}{\partial F} = \frac{\partial C_{BL}}{\partial F} + \frac{\partial C_{BL}}{\partial v} \frac{\partial v}{\partial F} = \Delta_{BL} + V_{BL} \frac{\partial v}{\partial F}$$
- $C_{BL}$ - Black scholes option price
- $\Delta_{BL}$ - black scholes delta
- $V_{BL}$ - Black scholes vega
- $\frac{\partial v}{\partial F}$ - Change in IV in a unit change in underlying
- Skew delta: $V_{BL}\frac{\partial v}{\partial F}$
	- Skew delta is unknown at T=0 -> 
	- $\frac{\partial v}{\partial F}$: the behavior of volatility at future price
- Ways to model the smile as futures keep moving intraday:
	- Heuristics
		- [[Sticky Moneyness]] - Basically tying vol to moneyness
		- [[Sticky Strike]] - basically Black-Scholes
	- [[Sticky Local Volatility]]
	- [[Quadratic Normal Model]]