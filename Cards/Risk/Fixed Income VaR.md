up:: [[Risk Management MOC]]
tags:: #Finance 
# Fixed income VaR
- Convert yields to prices with PV01
- position * PV01 * close * std of yield * 2.330 * 100
		- close -> extrapolates basis point move by this part: close * std yield * 100
	- 100 is for bps