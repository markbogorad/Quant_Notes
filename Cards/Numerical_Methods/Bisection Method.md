up:: [[Numerical Methods MOC]]
tags:: #Math
# Bisection Method
$$\text{MID} = \frac{\text{LO} + \text{HI}}{2}$$
- If $f(MID)≥0$, the root lies in the left subinterval, so $HI=MID$.
	- Otherwise, set $LO=MID$.
- a bracketing method that guarantees finding a root **as long as the function is continuous**, and **there is a sign change** between the initial interval $[LO,HI]$.
- **Advantages**:
	- Always converges for a continuous function with a root in the initial interval.
	- Simple to implement.
- **Disadvantages**:
	- Convergence is slow because it reduces the interval size by half at each step, requiring many iterations.
- **Application to Implied Volatility**:
	- The Bisection Method is particularly useful for [[Implied Volatility]] because it only requires the function values (not derivatives), which is helpful for functions like the Black-Scholes model.

![[Pasted image 20250126205746.png]]