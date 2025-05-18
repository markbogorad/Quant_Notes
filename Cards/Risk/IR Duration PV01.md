up:: [[Risk Management MOC]]
tags:: #Finance 
# Interest Rater Duration
- PV01 - dP/dy (rescaled to 1 bps)
		- Always is absolute value
		- To use for recent PnL attribution, multiply this value by the bps change in yields (ex: 4.55 to 4.58 - 3bp * D)
		- For historical - y_t-y_t-1 / yt - 1 = pct change yield 
			- **Scale them to todays level to take it form a relative return to absolute and apply duration**