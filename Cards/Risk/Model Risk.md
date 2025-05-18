up:: [[Risk Management MOC]]
tags:: #Finance 
# Model Risk
- Losses or suboptimal decisions (sometimes not purely financial) due to models inadequately or incorrectly preforming
	- Covers all topics where risk is larger than it should be
- All models are wrong, some models are useful
- Using a working model for similar things
	- Assumptions must become more stringent when you tailor to frequencies and such
	- Use a feeder model and then a core model
- Price Validation
	- Trying to match market prices with models by re-calibrating in real time
		- If no match - find out why
- Governance risk
	- Ensuring the people who make the models and the people who use the models are aligned
- Best model risk strategy is to hedge by buying and selling the same thing
## 3 lines of defense in model risk
- Business line (front line)
	- Model builders (devs) and model owners (traders)
- Model risk management MRM
	- Model validation
	- Test, review, monitor models
	- Re-implement the quants model with an independent implementation using a whitepaper by the quant
	- Stress test by adding shocks to the inputs
	- Makes sure people price products with models intended for those products
		- Re-certified once a year at least
- Internal Audit
## Option Model Risk
- Greeks Reporting for Model Risk
	- Greek is the amount of hedge you're taking
	- Interest rate exposures (Rho) is harder to hedge because its not very liquid
		- Large market players leave themselves unhedged
		- Best way to hedge this is with swaps
	- Gamma is unhedgable
		- If gamma is positive, you want to hold onto the transactions as long and possible (if vol increases youre making money)
		- Vega and gamma are naturally connected
			- When vega increases gamma decreases
		- If you have negative gamma, you will lose no matter what
		- Best way to get rid of Gamma risk is to sell the asset
### Flaws of Black Scholes
- No term structure
- Lognormal distribution
- Assumes hedging takes place continuously 
- Assumes no transaction costs ([[FVA]])
## Recording Model Risk
- Price-volatility matrices
	- A stress testing mechanism
	- If my price changes by X and my vol changes by Y, what will my price be?
	- See greeks as a product of this matrix
## Derman on Model Risk
- How to hedge illiquid positions
	- Have a pricing model to decompose mark to market risk
	- Build a suite of MC simulations going forward
		- Simulate behavior of trade and how we'd hedge it -> gives a distribution of outcomes 
	- This concept is "hedging to your model"
## Illiquid Positions
- Regulatory capital for illiquid positions
	- Regulators have you do stress test (macro, pro cyclaclcity, etc) and reprice
	- This is CCAR (doomsday scenarios)
- Hedge illiquid positions with liquid instruments to have more mobility in frequency
## Illiquid Swap Example of Liquidity Proxy
- ![[Screenshot 2025-05-12 at 11.28.43 AM.png]]
- Roll over your hedge to match horizons via swap
- Aka stack and roll