up:: [[Derivatives MOC]]
tags:: #Finance 
# Rho
$$\rho = \frac{\partial V}{\partial r}$$
- **Sensitivity of the option value to the interest rate used in [[Black-Scholes]]**
	- The aggregated risk exposure to interest rates changes for a book of options
	- For a 1% change in interest rates, option price will change by Rho
- In practice, a whole [[Term Structure of Interest Rates]] is used
	- Rho is the sensitivity assuming parallel shifts in the yield curve ([[Non-Parallel Shifts in the Yield Curve]] not captured!)
- In [[FX MOC]] options, Rho represents the sensitivity to foreign exchange
- Rho is adjusted on a firm portfolio basis to see [[Interest Rate Risk]]
	- Sum all Rhos and express as a P/L change per 1% interest rate change
	-  For example, if we have a rho risk of $2,000 we will make $2000 if interest rates move from 3.5% to 4.5% and lose $2000 if rates move from 3.5% to 2.5% instead.
- Borrowing money is long rho
- Lending money is short rho