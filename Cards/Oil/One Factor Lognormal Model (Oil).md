up:: [[Oil Markets MOC]]
tags:: #Finance 
# One Factor Lognormal Model
- A risk neutral approach where futures F(S,t) are priced under a risk neutral framework similar to the [[Black-Scholes]] [[PDE]]
	- Assume spot price follows a [[Geometric Brownian Motion]]
		- $\frac{dS}{S} = (r - y) dt + \sigma$
			- Y captures [[Convenience Yield]]
	- Apply [[Ito's Lemma]] to derive dF
		- $dF = \left( \frac{\partial F}{\partial t} + \frac{\sigma^2 S^2}{2} \frac{\partial^2 F}{\partial S^2} \right) dt + \frac{\partial F}{\partial S} dS$
	- Include [[Convenience Yield]] under no arbitrage
		- To ensure no-arbitrage, we consider a portfolio that consists of:
			- Holding one unit of the physical commodity S(t)
			- Shorting $\frac{∂F}{∂S}​$ futures contracts to hedge the price risk.
		- Return on hedged portfolio becomes
			- $dS + ySdt - \frac{\partial F}{\partial S} dF$
		- No Arbitrage condition becomes
			- $dS + ySdt - \frac{\partial F}{\partial S} \left( \frac{\partial F}{\partial t} + \frac{\sigma^2 S^2}{2} \frac{\partial^2 F}{\partial S^2} \right) dt = rSdt$
	- Derive the no arbitrage [[PDE]]
		- $\frac{\partial F}{\partial t} + \frac{\sigma^2 S^2}{2} \frac{\partial^2 F}{\partial S^2} + \left( r(t) - y(t) \right) S \frac{\partial F}{\partial S} = 0$
	- [[Boundary Conditions for PDEs]] - $F(S, T) = S$ at maturity (futures and spot match)
	- Solution
		- $F(S, t; T) = S e^{(r - y)(T - t)}$
## Pros
- Volatility is not constant; it decreases with time to maturity
- Different maturity futures can move in opposite directions
- Futures curve is not convex; it flattens with time to maturity