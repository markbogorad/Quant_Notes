up:: [[Fixed Income MOC]]
tags:: #Finance 
# Bond Payment Frequency
- EX: price of a bond
$$P = \sum_{t=1}^{N\cdot k} \frac{\frac{C}{k}}{(1 + \frac{r}{k})^{t}} + \frac{F}{(1 + \frac{r}{k})^{N\cdot k}}$$
- P = Current market price of the bond
- C = Annual coupon payment
- F = Face value of the bond (par value)
- N = Number of years until maturity
- k = Number of coupon payments per year (1 for annual, 2 semi annual, etc)
- r = Yield to maturity (YTM)
- t = Specific period within the total number of periods (from 1 to N⋅k)

- $\frac{C}{k}$​ is the periodic coupon payment (since there are k coupon payments per year).
- $(1+\frac{r}{k}​)^t$ adjusts the discount rate for the specific period $t$.
- $(1+\frac{r}{k}​​)^{N⋅k}$ adjusts the discount rate for the total number of periods, reflecting the compounding effect over multiple periods per year.
## Continuous Compounding
- Think of continuous time as  $\lim_{k \to \infty} \left(1 + \frac{r}{k}\right)^k = e^r$
- Therefore, as k approaches infinity (as time goes on), present value will be 
	- $PV = Ce^{-rt}$
	- more in [[Continuous Bond Price]]
	- 