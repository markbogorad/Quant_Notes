up:: [[Oil Markets MOC]]
tags:: #Finance 
# Time Spreads
- The spread of 2 adjacent futures through time
- Most popular quant thing to trade ([[Quantamental Oil Trading]])
## Practical Behavior
- In practice, many financial investors hold near maturity futures as a substitute for owning the actual commodity
	- With roll schedules public, traders are incentivized to front run and sell off time spreads ahead of the negative rolling pressure
		- Exacerbated in [[Concave Contango]], often causing **super contango**
![[Pasted image 20250116094036.png]]
## Time Spread Performance by [[Oil Curve Convexity]]
![[Pasted image 20250116095223.png]]

## Long-Short Spread Signal
- Sell and roll the prompt futures when curve is concave
- Buy when convex
$$\pi(S_{1-2,t})=sign(CV_{1-2-3,t})$$
- Where $S_{1-2, t} = F(t,T_1) - F(t,T_2)$ i.e. the spread