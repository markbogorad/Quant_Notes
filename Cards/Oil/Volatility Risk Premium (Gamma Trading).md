up:: [[Oil Markets MOC]]
tags:: #Finance 
# Volatility Risk Premium
- **VRP Strategy:** selling options and delta hedging them (selling insurance policies)
- **Option value depends on how you hedge it**
- Analogy: options are insurance with strikes as the deductible
- Volatility risk premium - expect to get paid for taking highly asymmetric risks
- Insurance companies price options actuarially ([[Quantitative Valuation MOC]]), dealers price with [[Delta Hedging]] framework (price is cost of delta hedging)
	- Unhedged (actuarial style) buyers make money and seller who is delta hedging is also making money
		- Both make money by trading with each other
## Oil Delta Hedging
- Volatility market makers price options this way
- PnL of the delta hedging strategy is [[Implied Volatility]] - [[Realized Volatility]] * [[Gamma]]
- Ideal delta hedge uses the correct [[Local Volatility]]
	- Hedging with [[Implied Volatility]] leaves residual risk from misspecification
- Gamma essentially highlights PnL sensitivity to to volatility mismatches
- Asymmetrical behavior for market makers -> need to buy/sell more options in adverse moves than in good moves to keep a delta neutral portfolio
- Delta hedging can also be seen as selling naked options and having an underlying in [[Oil Momentum Risk Premia]]
- Delta hedging for short gamma requires selling futures in price drops and buying in price increases
	- Counter momentum and psychological trading
## Strategy Performance
- VRP strategy works best for **deep out of the money options** the most, these tend to be overpriced the most as catastrophe insurance (never actually happen)
- On moneyness, premium retained is a bit higher for calls than puts
	- Explained by geopolitical risk premium (traders buying call protection against cataclysmic events in middle east)
- Long term options go negative fort deep OTM options
	- If long term options are cheap, you shouldn't be selling them

![[Pasted image 20250303203429.png]]
## Performance and Regime Changes
- 2000-2014 worked insanely well (>1 sharpe)
- Options financialization (2014-2020)
	- Packaged in a oil VRP index by banks -> more volatility supply
	- Index pays performance of strategy on a delta hedged basis -> used by shale producers (less demand)
![[Pasted image 20250303204246.png]]
## Optimizing VRP
- Default VRP is delta hedging, once a day on close, using Black-Scholes
- Optimizing
	- Adjust hedge frequency (hedge every X days)
		- Can wait out shake out moves with this frequency
	- Using a different delta -> different volatility -> different model
		- Calculate delta based on a volatility measure that aligns with your speculation
	
![[Pasted image 20250303203441.png]]
