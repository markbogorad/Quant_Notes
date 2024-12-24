up:: [[Derivatives MOC]]
tags:: #Finance 
# No Arbitrage Concept in Futures
- Futures prices follow an **exponential function** as time goes on ([[Exponential Distribution]]) by the principle of no arbitrage enforced by the market

![[Pasted image 20240625144126.png]]
## No Arbitrage:
- It must be true that $F_{0,T} = S_0 \times e ^{(r-\delta)t}$
- This just says the the forward price and the discounted spot price must converge, or else:
	- If $F_{0,T} > S_0 \times e ^{(r-\delta)t}$
		1) Borrow money
		2) Buy and hold the underlying at $S_0$
		3) Pay interest and get dividends, return money at a rate of $S_0 \times e ^{(r-\delta)t}$
		4) Sell stock at $F_{0,T}$
	- If $F_{0,T} < S_0 \times e ^{(r-\delta)t}$
		1) Short sell the underlying (borrowing $S_0$ and selling it for a net cashflow)
		2) Enter a futures to buy it back at $F_{0,T}$ (current forward rate for next period)
		3) Invest proceeds from (1) at the risk free rate to earn $r$
		4) Pay dividends $\delta$ to the owner
		5) Buy back the stock at time T at the forward rate agreed in (2), which didn't account for risk free compounding