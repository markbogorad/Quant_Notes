up:: [[Risk Management MOC]]
tags:: #Finance 
# MVA
- **Cost of having to be in a transaction via a central clearinghouse**
- Started in interest rate swaps because regulators are pushing swap trades to clearinghouses
- Step sister of CVA that results from transactions being pushed to central clearinghouses
- Initial margin vs variation margin
	- Variation margin is when trade is in place and valuations change, part of [[FVA-C (COLVA)]]
	- Initial margin is taken by exchange, a charge to account for potential collateral fluctuation during the 10 way window at default:
- Lore: there is a period of time between when the counterparty fails and the default is registered. Here you can liquidate collateral and initial borrowing to roll back the transaction. During this transaction, the central clearinghouses settles the trade under obligations of what is collateralized and what is not. Only day to day fluctuations are collateralized. Its fluctuation and there are 10 days where you can’t sell it. Valuation of collateral will fluctuate a lot during this period, and that is what initial margin is for. Initial margin protects you from fluctuations in this period. Its stashed away by another 3rd party.
	- Only happens with central clearinghouses, if dealing with a counterparty directly you have regular CVA
- MVA is 500x more expensive than [[CVA]]
	- Its 500 times more expensive to go through the exchange than to have an arrangement directly with the counterparty 
	- Dealing through an exchange gives you absolute insurance

## Formulaically
- Same as [[FVA]] just for margin instead of the portfolio
![[Screenshot 2025-05-11 at 5.00.18 PM.png]]
- Never need to do [[CVA]] on top
- $S_B (t)$ is the funding spread
- e^lambda is survival probability
- V(t) is the exposure
- e^r discounts it to present