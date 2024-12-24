up:: [[Fixed Income MOC]]
tags:: #Finance
# Convexity
- A more proper measure of bond price sensitivity
- Bond price sensitivity is convex
	- Whereas the [[Duration Model]] assumes it's linear
- Expressed in periods per year
	- $\text{Convexity in years} = \frac{\text{Convexity in } m \text{ periods per year}}{m^2}$
- High convexity (good for investors)
	- Bond price drops less when rates rise
	- Price drops more when rates fall
	
![[Pasted image 20240619153630.png]]

## Mathematically
$$\text{Convexity} = \frac{1}{P} \sum_{t=1}^{n} \frac{C_t \times t \times (t+1)}{(1 + y)^{t+2}}$$
- P is the current bond price
- C is the coupon cash flow
- t is the time period
- n is periods until maturity
- y is [[Yield to Maturity]]

- Also the 2nd derivative of a bonds price with respect to yield change
	- $\text{Convexity} = \frac{d^2P}{dy^2}$
- The higher the convexity, the higher is the bond price volatility

**Positive convexity**
- Most bonds have positive convexity
- Means that as interest rates increase, bond prices decrease (and vice versa)

**Negative convexity**
- For callable bonds [[Bonds with Embedded Options]], [[Bonds & Types of Bonds]]
- Bond price increases at a decreasing rate as interest rates fall and decrease at an increasing rate as rates rise (reread this sentence)

## Merging Convexity and Modified Duration to get a Sensitivity Measure
- [[Bond Price Sensitivity Using Convexity and MD]]



