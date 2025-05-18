up:: [[Risk Management MOC]]
tags:: #Finance 
# Bond Default Valuation
- To be averaged across a ton of simulations:
$$B_c(0) = c \sum_{i=1}^{N} \delta_i B(0, T_i) + B(0, T_N) + C(0; R)$$
- Bond default = sum of coupon payments + principal + recovery (all default adjusted)
- c = coupon rate
- δi​: The accrual factor for the i-th coupon period, accounting for the time length (like 0.5 for semi-annual).
## Principal Repayment Component
$$B(0, T) = \mathbb{E} \left[ 1_{\{\tau > T\}} \cdot e^{-\int_0^T r(u) \, du} \right]$$
- $1_{τ>T}​$ is an indicator that this takes value 1 if it survives and 0 otherwise
- If the bond **survives** until T, it will pay $1, but that payment must be **discounted back** to the present using the **risk-free rate**.
- If the bond **defaults before T**, it pays **nothing**, hence the indicator function ensures this.
Using hazard rate:
$$B(0, T) = \mathbb{E}\left[ e^{-\int_0^T \lambda(u) \, du} \right] <==>P(0, T)
= \mathbb{E}\left[ e^{-\int_0^T \left[ \lambda(u) + r(u) \right] du} \right]$$
## Recovery Amount
- Amount of residual assets that go back to bondholders (ranges wildly depending on company, sometimes 5% sometimes 90%. The usual number is 40%)
$$C(0; R) = \mathbb{E} \left[ \int_0^T R(s) \cdot \lambda(s) \cdot e^{-\int_0^s [\lambda(u) + r(u)] \, du} \, ds \right]$$
- Probability of survival * probability of defaulting at that exact point in time


## Coupons
- Coupons
	- Coupons have no recovery
	- Same pricing as principal repayment method just for each single coupon with a cutoff for the rest of the coupons at default time
$$c \delta_i \, \mathbb{E} \left( 1_{\{\tau > T_i\}} \cdot e^{-\int_0^{T_i} r(u) \, du} \right) = c \delta_i B(0, T_i),$$

