up:: [[Derivatives MOC]] [[Oil Markets MOC]]
tags:: #Finance 
# Implied Volatility ($\delta$)
- **A number you plug into the wrong formula to match the market price**
	- **Think of this as expressing option price in terms of strike and vol**
- The market's expectation of future volatility, derived from market prices 
	- Volatility: deviation of the underlying's price movement, measured by standard deviation of logarithmic returns ([[GARCH]])
		- The tighter the distribution, the lower the volatility
- Derived from [[Black-Scholes]] and other pricing models -> not observable
- The higher the implied volatility, the more expensive the contract
- Not constant throughout time -> [[The Volatility Smile]]
- Measure of price sensitivity to change in implied volatility -> [[Vega]]

## Volatility in Derivative Instruments
- Due to compounding, volatility follows a [[Lognormal Distribution]]
- ![[Pasted image 20240629160242.png]]
	- Capped at 0 for losses --> good for options and futures

## Calculating Volatility
- Daily volatility
	- $\text{expected 1 s.d. move over } t \text{ days} = \sigma \sqrt{\frac{t}{252}}$
- Resulting daily move
	- $\text{Expected Daily Move} = 0.8 \cdot \sigma \sqrt{\frac{t}{252}}$
	- 0.8 is the coefficient assuming 256 trading days (actually 252) for simplicity in calculations
- Historical volatility
	- $\text{vol} = \sqrt{\frac{252}{n} \sum_{j=0}^n \left( \log \frac{S_j}{S_{j-1}} \right)^2}$
	- The sum adds up the daily variances, dividing by n takes the average, and multiplying by 252 annualizes the average variance. This gives you the volatility
	- log returns used --> do not use levels (absolute) returns