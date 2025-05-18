up:: [[Oil Markets MOC]]
tags:: #Finance 
# Dynamic Theory of Storage
- The solution to the [[Robinson Crusoe Problem (Oil)]]
	- Models price as a function of availability (supply and demand)
	- If inventories are available, price are linked via [[The Carry Trade]] and we are in the investment regime (top formula)
	- If there is a stock out, the regime is driven by the inverse demand function and is called consumption regime
$$S(a(t)) = \begin{cases} 
F(a(t+dt)) - C(x), & \text{if } x_{\text{min}} < x < x_{\text{max}} \\ 
f^{-1}(a(t)), & \text{if } x = x_{\text{min,max}} 
\end{cases}
$$
-  $C(x)$ is total storage costs (known non-linear function)
- $F(a(t + dt)) - C(x)$: this is connected via the carry trade as long as there are inventories and storage (non grey area)
	- $a(t+dt)$ is an availability term. 
	- The carry trade here is buying and storing oil under $F(t,T)=S_te^{(r+c-y)(T-t)}$
	- If the futures price is too high, traders will buy S, store it, and sell futures contracts to lock in profits. This pushes the spot price up and the futures price down until the relationship stabilizes.  
	- Conversely, if the futures price is too low, they’ll sell spot oil and buy futures, pushing prices back toward equilibrium.
- $f^{-1}(a(t))$: this is the inverse demand function
	- This captures the bounds
- **Assumes 2 usages of oil, either carry trade or for consumption**
- Use [[Numerical Methods MOC]] to find S as a function of a -> that will be the optimal decision making policy
## The general price-inventory relationship
- Anywhere that isn't one of the boundary extremities, **oil price is insensitive to availability**
- Futures must equal spot + cost of storage

![[Pasted image 20250105165023.png]]
- If you have inventory, prices are no longer determined purely by economics - there is arbitrage via carry trade so futs = spot + storage
- Zero inventory state end shifts - that is the goal of the otpimal control problem
	- Zero inventory state - investment state
- Inverse demand function in 0 inventory state is extremely steep (consumption habits dont change with prices)
	- Demand so inelastic, we cant afford 0 inventories, therefore the solution is to store as much as possible
		- Cant store as much as possible because of storage capacity
	- This is the 2nd picture with steeper curves
		- [[Stylized Model of the Squeeze]]
- Trying to find the point where consumption region ends and investment region begins (blue dot)

## The Feedback Loop
Key relationships in the problem:
	 ![[Pasted image 20250211143224.png]]
- Price and quantity are related via inverse demand function
- Quantity today and tomorrow are related via the availability equation [[Robinson Crusoe Problem (Oil)]]
- Price today and tomorrow are linked via [[Cash and Carry Arbitrage]]
	- Need inventories for cash and carry, if inventories are not available, price is determined by inverse demand (the lower the inventory the higher the price)
- Storage essentially works as as an additional variable to [[Supply and Demand]], where you can pull in and out of storage to control he equilibrium

## Optimal Decision Making Policy
$$S(a(t)) = \max \left( E_t \left( S(a(t+dt)) \right) - C(x), f^{-1}(a(t)) \right)$$
- The **max operator** suggests that the decision-maker is optimizing between two competing factors:
1. **Expected future price minus costs** $Et(S(a(t+dt)))−C(x)$→ This represents the anticipated value of oil adjusted for storage costs.
	- Investment region
2. **The inverse demand function**$ f^{−1}(a(t))$→ This reflects how inventory levels determine prices based on supply/demand dynamics.
	- Consumption region
