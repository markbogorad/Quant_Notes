up:: [[FX MOC]]
tags:: #Finance 
# Covered Interest Rate Parity
	 $$1 + i_t = 1 + i + \frac{S_t - F_t}{S_t}$$
- Holds on the principle of no arbitrage
- **Principle:** 2 investments should have the same value
	1) A short term risk free asset (T-Bill)
	2) Exchange to FX and invest into a foreign T-Bill
	- $1 + i_t = 1 + i + \frac{S_t - F_t}{S_t}$
		- Domestic interest rate = foreign interest rate + the return on the hedge
			- Hedge position with a currency [[Forward Contracts]]
- Therefore:
	- $i_t - i_t^* - \frac{S_t - F_t}{S_t} = 0$
		- The interest rate differential - cost of the forward must be 0 or else there is arbitrage
## Arbitrage Principle
- If this relationship does not hold, one should be able to borrow at a cheap rate, invest at a high rate, and hedge this position with a forward perfectly
	- Essentially a perfectly hedged [[The Carry Trade]]
- These opportunities actually exist in practice
	- Many theorize it is a risk premium to counterparty credit risk involved in the 3 contracts