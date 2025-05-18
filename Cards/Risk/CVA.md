up:: [[Risk Management MOC]]
tags:: #Finance 
# CVA
- Adjusts the price down due to counterparty credit risk (they may default).
- Downward (negative) adjustment
- Computed using:
	- **Expected positive exposure (EPE)**
	- **Loss given default (LGD = 1 – recovery rate)**
	- **Default intensity / survival probability**
 - Basically priced as a [[Credit Default Swaps (CDS)]] just with a floating notional.
 - CVA is closely tied to the [[Credit Spreads (Hazard Rates)]]
	 - Higher the credit spread (premium above RF rate), the higher the CVA
## Unilateral CVA
- Assumes only the counterparty can default (you are default free i.e. a zero credit spread)
![[Screenshot 2025-05-11 at 11.46.43 AM.png]]
- 1-recovery -> how much you stand to lose (technically recovery is LGD here)
- First term (lambdas) -> PV of present exposure
- Second term -> PV of debt owed (only intended in positive valuation)
- Computing that on a portfolio that changes through time
- Default intensities, interest rates, are stochastic
- Not complex but needs creative thinking in modelling interest rates and intensities
- Its a massive [[Monte-Carlo Simulation]]
- Often a [[Dimensionality Reduction]] problem given high scope of fluctuating variables
- Many assume default and interest rates are independent but this is often not the case
	- Wrong way risk: the higher the rates (the more money companies make) the higher the default chances (more expensive to service debt for clients)
	- Right way risk: negative correlation between money making mechanism and probability of default (ex: oil producers and price of oil going up while their default goes down)
## Bilateral CVA
- Accounts for both parties possibly defaulting – requires conditioning on your own survival.
	- Very close to [[DVA]] -> you simulate your own default as well
	- Mechanic nuance -> adjustment becomes smaller than unilateral because you condition on it you having survived
		- Mechanically, if you collapse those simulations get cut off
![[Screenshot 2025-05-11 at 11.59.49 AM.png]]
- Extra term for your probability of survival
