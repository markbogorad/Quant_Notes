up:: [[Fixed Income MOC]]
tags:: #Finance
# Spot and Fwd Rates
- Spot rate is the annual interest you can lock in now (time zero)
- Forward rate is the implied rate of return from year 1 to year 2
	- Derived by creating a situation where you **buy the 2 year bond and finance it by selling the 1 year bond**
		- $B_2 - B_1 = Fwd_1$
- Spot rate is the average of the forward ratws
> "the forward rate is the single fixed rate in year 1-2 that gives us the same return as if we had bought a 1 year ZCB and reinvested the proceeds to receive exactly $1 at time 2. It is not the same as $r_{12}$ (a random variable) or even its expectation. It is the price of money from year 1-2 implied by bond spot prices that replaces the value of the unknown future cost." Shimko 62
## 2 Equivalent Investments
$$(1+r_0)(1+r_1) = (1+r_2)^2 = (1+r_0)(1+f_1)$$
- Rolling over 1 year spot = 2 year spot = 1 year spot + 1 year forward rate at t+1
