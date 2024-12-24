up:: [[Fixed Income MOC]]
tags:: #Finance
# Callable Bond
- Issuer has the right to call back the issue before maturity (retire the issue)
	- This is commonly exercised when interest rates fall below the coupon rate -> lower cost financing becomes available
- **Pricing:**
$$\text{Price of a callable bond} = \text{Price of an option-free bond} - \text{Price of a call option}$$
- [[Continuous Bond Price]] + [[Call Option]]

- **[[Convexity]] of a callable bond:**
	- ![[Pasted image 20240620174132.png]]
		- Becomes concave (aka price compression of a bond)
		- Limited price appreciation to the bond -> once high enough its going to be called back
# Putable Bond
- Bond holder (investor) has the right to sell the bond back to the issuer
	- Can be favorable if interest rates rise
		- Sell bond, reinvest money at new higher coupon bonds or buy cheaper bonds
- **Pricing:**
$$\text{Price of a putable bond} = \text{Price of an option-free bond} + \text{Price of a put option}$$
- [[Continuous Bond Price]] + [[Put Option]]

- **[[Convexity]] of a putable bond:**
- ![[Pasted image 20240620174719.png]]
	- Higher convexity -> pay premium for the put option
## Effective Duration and Convexity for Embedded Options
- [[Duration Model]], [[Convexity]]
- $\text{Effective Duration} = \frac{V_- - V_+}{2V_0 (\Delta y)}$
	- V is bond value
		- $V_-$ is the value if yields decrease, $V_+$ is the value if yields increase
	- y is the [[Yield to Maturity]] and here it represents the % change in YTM
- $\text{Effective Convexity} = \frac{V_- + V_+ - 2V_0}{2V_0 (\Delta y)^2}$
## Binomial Tree Valuation
- [[Lattice Methods]]
- ![[Pasted image 20240620175836.png]]
	- r is the interest rate
	- Objective is to find potential bond values due to changes in interest rate, solving at each node
#### Example:
- ![[Pasted image 20240620175934.png]]
	- Derive forward rates by assuming a standard deviation of x basis points
		- $\text{Rate}_H = \text{Rate}_L\times e^{N\times \delta}$
			- N = up move factor 
				- When h is 1, up move is 2. When h is 2, up move is 4
			- $\delta$ = standard deviation of interest rates
- If there is an embedded option:
	- Anything below par will be called or put: set it equal to par value:
		- Example (call):
			- ![[Pasted image 20240620180422.png]]
				- Set to 100 par
				- For a put, everything priced above 100 will be called back, therefore the ceiling is 100