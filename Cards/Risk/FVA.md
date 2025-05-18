up:: [[Risk Management MOC]]
tags:: #Finance 
# FVA-U
- The cost of _funding_ the cash needs of a derivative portfolio (transaction costs)
- While derivative trades are 0 at inception, they end up having changes and collateral obligations after
	- Traders don't have cash sitting around for this, finance it with [[Repo]]
		- The gap between return on asset and repo is the FVA (usually negative carry)
		- This isn't there implicitly because [[Black-Scholes]] assumes you can borrow and lend at the same rate
- Considered **desk-level,** not company-wide and for the lifetime of an entire trade on a trade-by-trade basis
- If you are short derivatives, you can have positive FVA (getting funding as income)
	- Would adjust the valuation up

![[Screenshot 2025-05-11 at 2.00.15 PM.png]]
- $S_B (t)$ is the funding spread
- e^lambda is survival probability
- V(t) is the exposure
- e^r discounts it to present
## Debt Overhang Connection
- Another way to think of it is a piece that measures your [[Debt Overhang]]
- The **cost of funding (FVA)** is effectively a **transfer of value to bondholders** (because they are owed the funding return), not shareholders.
- **FVA acts like a friction or tax** on trades that require external funding.  In highly levered institutions, this cost mostly **benefits debt holders**,  so **equity holders may underinvest** in profitable but capital-intensive trades.
- 
![[Pasted image 20250511170759.png]]
- New debt used to fund derivative positions takes a hit on equity holders (FVA is this cost to equity holders)


- [[FVA-C (COLVA)]]
