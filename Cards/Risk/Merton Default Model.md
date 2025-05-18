up:: [[Risk Management MOC]]
tags:: #Finance 
# Merton Model for Default
- A very similar structure to [[Black-Scholes]], just applied to the balance sheet
- Considers only 2 points in time t and T
## Setup
- $$A(t) = D(t) + E(t)$$
- $D(T) = A(T)-\text{max}(A(T)- D_F, 0)$
	- Final debt is just assets - notional value of debt 
- $E(T)=A(T)-D(T)=max(A(T)-D_F,0)$
	- Equity is just whats left over
- [[Real Options]] context
	- Debt holders are **short a [[Put Option]]** on the firms assets (limited upside with notional value of debt)
		- Limited upside in a no loss scenario
		- Large downside
	- Equity holders hold **a long [[Call Option]]**
	- Volatility for balance sheets - volatility of stock proxy (sometimes times regression factor)
	- $A(0)$ is the underlying spot equivalent
	- $D_F$ is the strike
$$E(0)=A(0)*N(d1)-D_Fe^{-rT}*N(d2)$$
- This gives the fair price of a firms assets
$$d1=\frac{ln(\frac{A(0)}{D_F})+(r+0.5\sigma^2_A)*T}{\sigma_a\sqrt{T}}$$
- $\sigma_A$ is asset vol
- Probability of survival = $P(A(T)>D_F)=N(d_2)$