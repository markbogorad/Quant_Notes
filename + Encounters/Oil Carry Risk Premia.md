up:: [[Oil Markets MOC]]
tags:: #Finance 
# Commodity Carry
- [[Algorithmic Trading in Oil]]
- Stems form theory of storage ([[Dynamic Theory of Storage]])
- Model independent strategy
- Transmitter of fundamentals to prices
	- *Transmits information via behavior of hedgers*
- The systematic traders synonym for [[Oil Own Rate]] or [[Convenience Yield]]
## The Carry
- The carry is essentially the status quo (betting on nothing changing)
	- Trading on the probability of nothing changing (spot price and futures curve) and you rolling futures up or down the curve
	- Risk premium is the (spot - futures) spread
- [[The Carry Trade]] can be extended from FX to various asset classes
	- In equities carry is dividend yield
## Trade Strategy
- [[Contango & Backwardation Markets]]
	- When in contango, long carry is ideal
	- When in backwardation, short carry is ideal
- Signal
$$C_t(M,N)=F_{t,M}-F_{t,N}, M<N$$
- Wether the increment in the change of futures as you go out into maturity is positive or negative
	- Positive --> contango --> long carry, and vice versa
- Common length is 1 year (12 months of data) carry to eliminate seasonal effects
	- 20.3% return with sharpe 0.53
	
![[Pasted image 20250115101107.png]]
## Pros and Cons
- Model independent -> less room for error
- Unable to react to rapidly changing conditions, i.e. a change in the futures curve
## Dynamic Carry Alternative
- Combining with the [[Oil Momentum Risk Premia]] factor, i.e. an [[MA]]
$$\pi_{CM}(F_t)=sign(C_t-MA_t(C_t;n))$$
- Has 24.7 annualized returns and 0.64 Sharpe over 30 years