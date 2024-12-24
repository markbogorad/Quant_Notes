up:: [[Fixed Income MOC]]
tags:: #Finance
# Hedging with Bonds
- Goal: protect an investor who is unsure of future [[Yield Curve]] changes
- Strategy: take an opposite position to what you have in your portfolio
- Key:
	- Hedges are not symmetric
		- $\text{Hedge for long bond 1 short bond 2 } \neq \text{ hedge for short bond 1 long bond 2}$
	- Hedges are not transitive
		- If bonds A, B, C hedge work, this does not mean A and C will work or C and A
		- ![[Pasted image 20240621124145.png]]
## Conventional Hedge
- Only works if yield curve shift is parallel
- Hedge to match long and short **position weights**
- $Q_2 = -\frac{V_1}{V_2} \times Q_1$
	- $Q_1$ and $Q_2$ are the values of the positions (here 1 is long 2 is short)
	- V is the [[Price Value of a Basis Point]]
	- Negative in this case because it represents the short position on $V_2$
- Issues
	- Requires perfect correlation in yield changes between the bonds
		- Will cause an over-hedge
## Optimal Hedge 1 Bond
- Protects from level changes in interest rates
- Factors in volatility of yields and prices, as well as bond correlations
- Optimal hedge:
	- $\Delta W = Q_1 V_1 \Delta v_1 + Q_2 V_2 \Delta v_2$
		- Q is principal amounts of the bonds
		- V is [[Price Value of a Basis Point]]
		- 1 refers to bond position we want to hedge
		- 2 refers to the bond we are using to hedge the original position
			- $Q_2 = -\frac{\rho_{1,2} V_1 \sigma_1}{V_2 \sigma_2} Q_1$
				- Ideally correlation ($\rho$) will be 1
				- $\sigma$ is volatility

## Optimal Hedge 2 Bonds
- Protects from level changes in interest rates + [[Non-Parallel Shifts in the Yield Curve]]
- $\Delta W = Q_1 V_1 \Delta y_1 + Q_2 V_2 \Delta y_2 + Q_3 V_3 \Delta y_3$
	- $Q_2 = -\frac{(\rho_{1,2} - \rho_{1,3} \times \rho_{2,3}) V_1 \sigma_1}{(1 - \rho_{2,3}^2)^{1/2} V_2 \sigma_2} Q_1$
	- $Q_3 = -\frac{(\rho_{1,3} - \rho_{1,2} \times \rho_{2,3}) V_1 \sigma_1}{(1 - \rho_{2,3}^2)^{1/2} V_3 \sigma_3} Q_1$
	- where
		- Q2 must have a shorter maturity than Q3
			- Shorter maturity ensures that one side benefits from the flattening or steepening