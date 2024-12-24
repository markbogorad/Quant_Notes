up:: [[Derivatives MOC]]
tags:: #Finance 
# Outright Trading Window
- Similar to [[Option Chain Quotes]]

![[Pasted image 20240627150235.png]]

- Expiry on top 2-22-19
- [[Call Option]] on left
- [[Put Option]] on right
- Gray bids and ask boxed --> outside of bid/ask range so [[Market Makers]] won't participate
- To the left (or right) of bid (or ask)
	- This number is how many contracts the market is willing to buy at that given price
		- ex: 109 contracts for the 0.125 bid (740 strike)
- Left most column: **turnover quantity** for calls (CTO) and (PTO for puts on the right side)
	- How many contracts have traded today
- **Spline delta** --> orange row
	- [[Delta]] for each contract
	- Highlighted in orange are [[Delta]]s closest to volatility curve ([[The Volatility Smile]])
		- Helps traders see where strikes fall in delta space
- Purple column is the position column (T Pos)
	- What positions the [[Market Makers]] hold
- [[Vega]] on the far right
- **Bid offset** --> furthest right
	- Bid offset is the edge we require to keep trading the theo (theoretical price)