up:: [[Risk Management MOC]]
tags:: #Finance 
# Coherence Measure
- [[Value at Risk (VaR)]] is NOT subadditive, [[Expected Shortfall (ES)]] IS
	- Happens because it ignores tail dependencies -> the sum of 2 VaRs can be be higher than the sum of the individual VaRs, which is bad

Coherence measure - if something is not coherent it will break in a different market enviroment
**4 conditions:**
- Monotonicity: If Y dominates X in every stat, it is less risky
	- If one portfolio achieves higher returns in every state, it has lower risk
- Translation invariance - if you move part of portfolio to cash, it should reduce risk (**adding cash reduces risk**)
- Positive homogeneity - **risk is proportional to size** (does not consider liquidity)
	- Portfolio size will move market (lambda position)
- **Subadditivity** - portfolio should not exceed sum of risk of each asset (negative diversification)
	- Most important measure of the 4


- ![[Screenshot 2025-03-19 at 11.25.52 AM.png]]