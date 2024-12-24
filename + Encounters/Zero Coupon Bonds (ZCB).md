up:: [[Fixed Income MOC]]
tags:: #Finance 
# ZCBs
- A bond that doesn't pay an coupons
- Often used to derive the yield curve with ZCB [[Bootstrapping]]
	- Deriving future expectations of the yield curve by plotting ZCBs at various expries
## ZCB Valuation
$$P = \frac{F}{\prod_{i=1}^n \left(1 + \frac{r_i}{m}\right)^m}$$

- F is the face value of the bond,
- $r_i$ is the discount rate for period i,
- $m$ is the number of compounding intervals within each period (e.g., $( m = 2)$ for semiannual, $( m = 4)$ for quarterly),
- n represents the total number of years to maturity.
