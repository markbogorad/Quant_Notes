up:: [[Fixed Income MOC]]
tags:: #Finance
# Butterfly Trade
- Concept: swap a bond for a portfolio of bonds (short a bullet and long a barbell) [[Bond Portfolio Strategies]]. By swapping bonds back and fourth, investors seek to exploit movements in the yield curve
- Goal: enhance yield and improve [[Convexity]]
- Key: aggregate risk of bullet and barbell must match
## Weighting Methods
### Cash Neutral Butterfly 
- Most common weighting method
- Conditions:
	- Purchase cost of barbell portfolio must counterbalance proceeds of short sale **(cash neutrality)**
	- Risk ([[Duration Model]]), must be equal in the short and long position

### 50-50 Duration Method Butterfly
- Risk neutral trade
- Place 50% of the dollar duration in each wing ([[Duration and Modified Duration Model Variants]])
	- $\text{Duration of bullet} = \text{Duration of barbell}$
- Only works well for small shifts in the yield curve
	- Does not account differing volatility between bullet and barbell

### Regression Method Butterfly
- Regress the spread between long and medium term bonds to account for volatility
	- $\Delta S_{l-m} = \alpha + \beta \Delta S_{m-s} + \epsilon$
		- Beta here shows the change in short term yield vs change in long term yield
			- Ex: beta = 0.65 → a 1% change on the short end leads to a 0.65% change on the long end
- Durations must match
- Volatilities must match
	- ![[Pasted image 20240620211434.png]]
- 
