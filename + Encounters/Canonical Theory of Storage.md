up:: [[Oil Markets MOC]]
tags:: #Finance
# Canonical Theory of Storage
 - Some [[Economics MOC]] framework
	 - Just considers oil storage as a function of supply and demand, which affects the commodities price
		 - High supply = lower price & all the other economic implications
		 - Out of inventory: called a *stock out*
		 - Too much inventory: *tank tops*
- Considers boundary effects
	- Bottom: zero inventory
		- The closer you are to this, the higher the [[Convenience Yield]]
	- Top: constraint on storage
- Formula: flow of inventories is equal to the difference in supply today $(Z(t))$ and demand $(D(t))$
	- $x(t) - x(t-dt) = Z(t) - D(t)$
		- Z(t) is the sum of local production and imports from other regions
			- Supply is an uncertain figure and demand is is deterministic
		- D(t) is total consumption and exports
## Cumulative level of inventories
$$0 < X_{min} \leq x(T) \leq X_{max} < X$$
$$x(T) = x(t) + \int_t^T (Z(t) - D(t)) dt$$
- $X_{min}$: a minimum operating capacity
- $X_{max}$: maximum operating capacity
## 2 State Equation
$$S(a(t)) = \begin{cases} F(a(t + dt)) - C(x), & \text{if } X_{\min} < x < X_{\max}, \\ f^{-1}(a(t)), & \text{if } x = X_{\min}. \end{cases}$$
- $C(x)$ is total storage costs
- $F(a(t + dt)) - C(x)$: 
- $f^{-1}(a(t))$: this is the inverse demand function, representing
## Solving in Practice
- Code it as a stochastic dynamic programming problem ([[Python MOC]])

## The general price-inventory relationship
- Anywhere that isn't one of the boundary extremities, **oil price is insensitive to availability**

![[Pasted image 20250105165023.png]]
