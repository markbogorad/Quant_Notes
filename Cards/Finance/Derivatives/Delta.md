 up:: [[Derivatives MOC]]
tags:: #Finance 
# Delta
$$\Delta = \frac{\partial V}{\partial S}$$
- **Sensitivity of option price to the underlying**
	- The rate of increase in the option position per unit increase of the underlying

- Delta is an estimate derived from [[Black-Scholes]], and therefore does not set in stone your price variability per unit increase
	- Can make risk management very difficult in options trading as there are no concrete stop losses or take profit orders
- [[Delta Hedging]] means this number should be 0, and the option price will be immune to stock price changes

- In general: the lower the delta, the lower the chances of finishing in the money
	- Any delta at 50 or below: out of the money
	- Any delta at 50 or above: in the money

- Call deltas: from 0 to 1
- Put deltas from 0 to (-1)
- Call and put deltas are symmetrical (equal 1) in absolute value
	- Ex: call delta = 0.18 and put delta = -0.82 --> absolute value is 1
	- *Intuition:* adds up to 100% chance of options being in the money

## Market Makers Point of View
- **Hedge ratio:** Another way to think of Delta (from [[Market Makers]] view): *the number of underlying contracts* that allow for a neutral hedge under current market conditions (using theos)
	- Commonly spoken of in contract size, ex: (delta of 0.57 is verbalized as 57, and is the amount of contracts we'd need for a hedge under every 100 contracts we trade)

## Delta and Factors that Influence it
- [[Implied Volatility]]
	- The higher the implied volatility, the higher the chances of being in the money (until 50%), the higher the delta, the higher the option price
		- Delta will approach 0.50 for calls, and -0.50 for puts
- Time to Maturity
	- The longer the time to expiry, the more time the option has to move around and become ITM
		- Delta will approach 0.50 for calls, and -0.50 for puts
- Strike Prices
	- Call: Deltas decrease as strikes increase
	- Put: Deltas increase as strikes increase

## Cash Delta
- $\text{Cash Delta} = \text{Underlying Price} \times \text{Multiplier} \times \text{Quantitiy of Futures}$
- Similar to edge but for Deltas