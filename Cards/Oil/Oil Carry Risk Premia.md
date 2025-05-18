up:: [[Oil Markets MOC]]
tags:: #Finance 
# Commodity Carry
- [[Algorithmic Trading in Oil]]
- Exploiting the futures - spot convergence behavior in [[Contango & Backwardation Markets]] based on [[Dynamic Theory of Storage (Price-Inventory Feedback Loop)]]
- **A model independent strategy (parameter free)**
	- Buy futures, sell oil in backwardartion
		- As long as difference between spot and futures covers cost of storage it works
		- Here, storage owners are pulling oil out of storage and selling to the consumer 
	- Buy oil, sell futures in contango
		- Pull oil out of storage and buy back futures
		- As long as we're in contango, the storage owners are always going to be selling futures
- Market is backward when short term contract exceeds long term
- Market is contango when long term contract exceeds short term
- **Essentially front running storage traders (largest traders in the market)**
	- Transmitter of fundamentals to prices
		- *Transmits information via behavior of hedgers*
		- The systematic traders synonym for [[Oil Own Rate]] or [[Convenience Yield]] is carry
## Trade Strategy
- Signal
$$C_t(M,N)=F_{t,M}-F_{t,N}, M<N$$
	**- Market is backward when short term contract exceeds long term**
	**- Market is contango when long term contract exceeds short term**
- Looks whether the increment in the change of futures as you go out into maturity is positive or negative
	- Positive --> contango --> short carry, and vice versa
- Common length is 1 year (M1 M13 months of data) carry to eliminate seasonal effects $C_t(1,13)$
	- 20.3% return with sharpe 0.53
- Adding an epsilon parameter as a threshold can help improve returns because you'd only trade when the curve is covnex enough
	- [[Convex Backwardation]]
	
![[Pasted image 20250115101107.png]]
## Pros and Cons
- Model independent -> less room for error
- Unable to react to rapidly changing conditions, i.e. a change in the futures curve
## Dynamic Carry Alternative (Blended Signal-2nd Order Trading)
- Combining with the [[Oil Momentum Risk Premia]] factor, i.e. an [[MA]]
$$\pi_{CM}(F_t)=sign(C_t-MA_t(C_t;n))$$
- If todays carry exceeds the moving average carry, buy
	- **Effectively buying when backwardation accelerates (steepens) and sell when backwardation decelerates (gets flatter)**
	- **Contango gets steeper - sell, contango gets flatter - buy**
- Has 24.7 annualized returns and 0.64 Sharpe over 30 years
- AKA basis momentum - famous paper on this