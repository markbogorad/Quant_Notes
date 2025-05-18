up:: [[Oil Markets MOC]]
tags:: #Finance 
# Sticky Strike
 - Not a recommended way to do it
 - Forcing volatility to stick to the strike (i.e. the vol will follow strikes as other parameters change)
	 - Forcing vol to be the same for every strike
	 - Every strike must have a certain volatility regardless of moneyness
		 - Essentially turning it into Black Scholes at multiple strikes (const vol assumption)

![[Pasted image 20250304132727.png]]

## Why its bad
- You have the natural lognormal asymmetry from Black-Scholes throwing you off