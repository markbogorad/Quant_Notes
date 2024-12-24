up:: [[FX MOC]]
tags:: #Finance 
# Uncovered Interest Rate Parity
$$1 + i_t = 1 + i_t^* + \frac{S_{t+k}^e - S_t}{S_t} + rp_t \hspace{1cm} OR \hspace{1cm} i_t - i_t^* = fp_t = \frac{S_{t+k} - S_t}{S_t} + e_t$$
- Same concept as [[Covered Interest Rate Parity]] except we no longer hedge
	- This is not arbitrage anymore, we are taking a risk
- **Principle:** the interest rate differential is mean't to be equalized by the depreciation of the foreign currency
	- Ex: domestic is UK 5%, foreign is US 7%
		- Can expect the USD to depreciate by 2%
	- Under this assumption, the forward rate becomes an unbiased ([[Unbiasedness (Estimators)]]) forecast of exchange rates
		- Fails in practice: its actually random