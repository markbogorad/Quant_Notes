up:: [[Oil Markets MOC]]
tags:: #Finance 
# Sticky Local Volatility
- Leveraging the average and slope relationship between local volatility and implied volatility
- [[Implied Volatility]] is approximately the average of [[Local Volatility]] over stochastic paths from todays future price to the strike price
	- IV can be approximated as average of local vol
- Locally, the slope of IV is roughly 1/2 of the slope of local vol
- Theory - we know the stochastic process that will match the smile. We use this process to basically predict skew delta
$$\sigma(F)=v_0-2\beta(F-F_0)$$

![[Pasted image 20250304133912.png]]
- The heuristics are producing the forward behavior of the smile

## Pros Cons
- Delta hedge is in the right direction - no asymmetry as from [[Sticky Strike]] or [[Sticky Moneyness]]
- 