up:: [[Oil Markets MOC]]
tags:: #Finance 
# Rolling Futures
- Roll contracts on final day of month - academic approach
- Roll contracts X days before expiry - practical approach
## An example
- S(t) = 60
- F(t, t+1) = 59
- S(t+1) = 70
- F(t+1, t+2) = 68
- S(t+2)= 65
- F(t+2, t+3) = 65
- Spot PnL: 60 -> 70 -> 65 = 10 - 5 = 5
- Rolling futures PnL: 59 becomes 70 (+11), buy 68 which becomes 65 (-3) = 8
	- FPL (t+1) = S(t+1) - F(t, t+1) = 70-59 = 11
	- FPL (t+2) = S(t+2) - F(t+1, t+2) = 65-68 = -3