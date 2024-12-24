up:: [[Banking MOC]] , [[Fixed Income MOC]]
tags:: #Finance 
# Duration Model (Macaulay Duration)
- *A method to measure price sensitivity*: [[Interest Rate Risk]] or [[Fixed Income MOC]] price sensitivity
- Measures time to receive all cash flows
	- Essentially a weighted average of time to maturity using relative PVs
- General rules
	- Longer maturity = greater sensitivity
	- Lower coupons = greater sensitivity 
	$$ D = \frac{\sum_{t=1}^{T} t \cdot \frac{C_t}{(1+y)^t}}{P} $$
	where:
	- t is the time period in years
	- Ct is the cash flow at time t (including coupon payments and principal repayment)
	- y is the [[Yield to Maturity]] (YTM) of the bond
		- If time period is lower then years divide y (ex: semi-annual = y/2 and Tx2) 
	- P is the current price of the bond
	- T is the total number of periods (years) until the bond's maturity
	
	- D is the duration *in years by default*
	- **Even simpler formula:** Sum of all (cash flow * discount factor * time) / (cash flow * discount factor)
## Relationships
- Maturity increases --> duration increases (at a decreasing rate due to convexity)
- YTM increases --> duration decreases
- Coupon interest increases --> duration decreases

## Modified Duration
- Measuring sensitivity of an asset to changes in interest rates (*interest rate sensitivity*)
- Used practically in finance (Macaulay used in academics)
$$ D = \frac{M}{(1+\frac{y}{n})} $$
- M = Macaulay Duration
- y = YTM
- n = compound periods per year (usually just 1)

- D = % change in price per 1% change in yield
	- Assumes a linear relationship, but reality is convex -> [[Convexity]]
		- ![[Pasted image 20240619153618.png]]