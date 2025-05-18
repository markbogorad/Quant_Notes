up:: [[Oil Markets MOC]]
tags:: #Finance 
# Local Volatility
- This is the actual thing thats in stochastic processes (the actual functional coefficient)
- Graphed **in terms of the underlying** (implied vol is in terms of strike)
$$\sigma (F,t)$$
- Describes empirically how the world works (volatility in strike-time space)
- Local volatility is a point on the [[Implied Volatility]] surface -> (strike, time)
- Unlike implied volatility, which reflects the market’s average expectation, local volatility gives granular insight into how volatility behaves dynamically.
- Derived using the Dupire equation, which differentiates the implied volatility surface:
$$\sigma_{\text{local}}^2(S, t) = \frac{\frac{\partial C(S, t)}{\partial t} + r S \frac{\partial C(S, t)}{\partial S}}{\frac{1}{2} S^2 \frac{\partial^2 C(S, t)}{\partial S^2}}$$
- Local volatility = [[Theta]] + carry cost due to risk free interest $/$ [[Gamma]]
	- ${\frac{\partial C(S, t)}{\partial t}}$ - theta
	- $r S \frac{\partial C(S, t)}{\partial S}$ - carry cost
	- ${\frac{1}{2} S^2 \frac{\partial^2 C(S, t)}{\partial S^2}}$ - gamma
## When to use
- When working across time and strike - this is necessary for no arbitrage pricing
## Relationship between Local and Implied Vols
- Implied volatility is approximately the average of local volatility over the paths that go from todays futures price to the final strike
	- **Implied volatility can be approximated as average of local volatility**
	- **Slope of implied volatility is roughly 1/2 of local volatility**
	- **Convexity of implied volatility is roughly 1/3 of local volatility**
![[Pasted image 20250309105752.png]]
- Ex: if you want implied vol at strike 30, you take the integral (average) local volatility from 60 (ATM) to 30