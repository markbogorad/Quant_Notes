up:: [[Oil Markets MOC]]
tags:: #Finance 
# Robinson Crusoe Problem
- Uses Bellman equation in stochastic optimal control to work backwards and find the optimal decision
	- Builds on [[Canonical Theory of Storage]]
- Key logic: how much to consume today vs how much to consume tomorrow
	- This essentially creates conditions that replicate convenience yield behavior
	- Idea: presence of the extreme boundaries should have an impact on the middle of the working curve [[Canonical Theory of Storage]]
$$x(t) - x(t-dt) = \tilde Z(t) - D(t)$$
- Where
	- Z(t) is the sum of local production and imports from other regions (unknown variable)
		- Supply is an uncertain figure and demand is is deterministic
	- D(t) is total consumption and exports
	- If supply exceeds demand (Z>D), that will be equal to the change in [[Oil Inventories]], storage is the **balancing mechanism**
		- If supply is greater than demand, you add to storage
		- If supply is less than demand, take oil out of storage
- **Integrating** this over time results in the aggregate level of inventories: storage at time T = initial storage + cumulative difference between supply and demand over a certain period
$$𝑥(𝑇) = 𝑥(𝑡) + \int_t^T (\tilde Z(t) − D(t) 𝑑𝑡)$$ 
- Boundary is:
	- $X_{min}$: a minimum operating capacity
	- $X_{max}$: maximum operating capacity
	- 2 boundary stochastic control problem [[Stochastic Calculus MOC]]
$$0 < 𝑋_{𝑚𝑖𝑛} ≤ 𝑥(𝑇) ≤ 𝑋_{𝑚𝑎𝑥} < 𝑋$$
- **Availability** of oil can be defined as: whatever you get today (supply) + whatever you carry from yesterday
	- Availability today a(t) - how much you consume today D(t) + how much you store for future Z(t+dt)
$$𝑎(𝑡 + 𝑑𝑡) =\tilde{𝑍} (𝑡 + 𝑑𝑡) + 𝑥 (𝑡) = 𝑎 (𝑡) − 𝐷 (𝑡) +\tilde𝑍 (𝑡 + 𝑑𝑡)$$
- 