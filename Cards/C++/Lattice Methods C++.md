up:: [[C++ MOC]]
tags:: #Programming
# [[Lattice Methods]] C++
### Uses:
- Particularly useful for American options
- Not most accurate
	- Oscillates depending on time steps
## Processes
### Forward induction
- Going from 0 to time T
	- Creates the binomial price tree
### Backwards induction
- Going from time T to 0
	- Compute price by going backwards
## Stochastic Differential Equation:
### SDE Formula:
$$
dS = \mu Sdt + \sigma SdW
$$
where:
	$\sigma$ = volatility
	$\mu$ = drift
	dW = Brownain motion (Wiener Process)
	d = down jump value
	u = up jump value
	$p_u$ = probability that the asset price is uS
	$p_d$ = probability that the asset price is dS
### SDE Up/Down State Valuation
CRR: Cox Ross Rubenstein![[Screenshot 2024-03-28 at 11.20.33 AM.png]]

JR: 
![[Screenshot 2024-03-28 at 11.20.38 AM.png]]

## How it works:
> Based on Clewlow and Strickland 1998
- Note: 
	- Never want to hardd code these formulas, you want some kind of flexibility so you can change models at runtime
- Classes:
	- Lattice class
		- Full nested vector class (the lattice itself is a vector of a vector, akin to a matrix)
		- Components:
			- Template class with 3 variables (V for vector, I for rows (iterations) N for number of nodes)
			- Canonical header
			- Iterations members (forward, backward, depth)
			- = operator
			- subscript operator
			- Base of the lattice pyramid
	- LatticeFactory class
		- Abstract factory for creating a binomial lattice
		- Components
			- All variables of binomial pricing (u, d, p, s, r, k)
			- Up/down state calculation methods (CRR, JR, EQP, TRG, ModCRR)
	- Option class
		- Class for the call/put payoff (max S-K, 0)
		- Components
			- Interest rate, volatility, strike price, expiry date, underlying, cost of carry, option type (1 for call 2 for put ex)
	- EuropeanOptionFactory class
		- Class used to enter inputs of "Option Class" variables
		- Components
			- Pure virtual function : Option* create()
			- Separate class for `cin` and `cout` at each variable from option class
	- BinomialMethod class
		- Mediator between the lattice tree (data structure) and different algorithms (CRR) for initializing the tree
		- Components
			- Canocnical header
			- Initialize lattice
			- Forward induction
				-  Calculate derivative price
			- Backward induction
				- Calculate derivative price
	- BinomialLatticeStrategy
		- Creates actual binomial lattice
		- Components
			- Protected variables: binomial pricing variables (u, d, p, s, r, k)