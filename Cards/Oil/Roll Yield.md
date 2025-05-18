up:: [[Oil Markets MOC]]
tags:: #Finance
# Roll Yield
- Concept: trying to approximate the spot price of oil by buying nearest maturity future and rolling it
	- Tying to synthesize the continuous ownership of barrels by holding and rolling futures
- **Foundational equation:**
$$ER(T)=ln(\frac{S(T)}{S(t)})+ln(\frac{S(t)}{F(t,T)})$$
	- Excess return = spot return + roll return
		- Same formula over cumulative (sums of returns)
- **Final formula**
$$j=\frac{1}{T-t}ln(\frac{S(t)}{F(t,T)}) \text{ - - - EQUALS - - - } F(t,T)=S(t)e^{-j(T-t)}$$
	- Divide by time to maturity to annualize
## Roll yield, convenience yield, own rate
- The relationship between roll yield, [[Convenience Yield]], and [[Oil Own Rate]] is:
$$j=b-r=y-u-r$$
- Can be thought of as the spread between oil own rate and USD own rate (interest rate)
	- Also convenience yield net storage and interest costs
## Spot vs Roll Returns Logic
- Spot doesn't exist unless you own storage
- In practice, traders roll futures by entering M2 futures a few days before expiry (not to get caught with delivery), hold M2, until it expires, then it becomes M1. Those 5 days and the transaction costs can change the PnL vastly
- If the curve is in Contango ([[Contango & Backwardation Markets]]), there will be a negative roll yield