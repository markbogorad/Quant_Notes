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