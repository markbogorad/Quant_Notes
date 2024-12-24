up:: [[Derivatives MOC]]
tags:: #Finance 
# [[Delta]] Hedging
- Keeping the portfolio delta figure at 0
	- $\Delta = \frac{\partial V}{\partial S}=0$
		- This is also known as "delta neutral"
- Works because it exploits perfect correlation between the underlying and the option
- Delta hedging is a continues readjustment, also known as rebalancing
	- Often results in losses due to constant rebalancing and transaction costs
- You can also delta hedge with an entirely different position
	- If you have two instruments with inversely proportional deltas
	- Exposed to [[Basis Risk]]

## How Market Makers Determine Hedges
- Split up the options multiplied by their exposure, then derive an equal counter hedge
- Goal: maintain a portfolio that is insensitive to moves in the underlying

![[Pasted image 20240629114653.png]]