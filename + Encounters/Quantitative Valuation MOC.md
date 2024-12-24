up:: [[Home]]
tags:: #MOC 
# Quantitative Valuation Methods
## GVE
- [[Valuation Models]]
- [[Implications of Limited Liability on Valuation]]
- [[Elon Musk Problem]]
- [[Opportunity Cost (Valuation)]]
- [[General Valuation Equation (GVE)]]
	- [[GVE Simple Computations]]
	- [[GVE Fixed Income]]
	- [[GVE Event Based]]
	- [[GVE Stochastic Processes]]
	- [[GVE Correlated Cash Flows]]
	- [[GVE Risk Introduction]]
	- [[GVE Futures & Forwards]]
- Risk Neutral Pricing
## Financial Assets & Contracts
- [[Financial Asset vs Contract]]
- [[Discounting and Compounding Frequency Mismatch]]
- [[Fisher Equation (Inflation)]]
- [[COLA]]
- [[FX Quote]]
	- [[Covered Interest Rate Parity]]
	- [[FX Rates and Forwards]]
- [[Bonds & Types of Bonds]]
	- [[Floating Rate Note (FRN)]]
	- [[Bond Spot and Forward Rate Relationship]]
	- [[Yield Curve]]
		- [[Bootstrapping]]
	- [[Effective Annual Yield]]
	- [[Bond Equivalent Yield]]
	- [[Zero Coupon Bonds (ZCB)]]
	- [[Forward Bond]]
	- [[Accrued Interest on a Bond]]
- [[Loans Amortization]]
- [[CDO]]
- ETFs
- [[Futures and Forwards in Valuation]]
	- [[Futures Contracts]]
	- [[Forward Contracts]]
	- [[Cash and Carry Arbitrage]]
	- [[Financial vs Non-Financial Forwards]]
	- [[Margining Risk]]
	- [[Contago & Backwardation Markets]]
- Options
	- [[Implied Volatility]]
	- [[Implied Probability]]
	- [[Mixing Distributions]]
## Simulation
- [[Simulation in Finance]]
- [[Creating Z Values (Inverse CDF)]]
- [[Variance Reduction Techniques (Simulation)]]
	- [[Antithetic]]
	- [[Moment Matching]]
		- [[Cholesky Decomposition]]
	- [[Control Variate]]
- [[Multivariate Simulation (Correlating Cash Flows)]]
	- [[Copulae (Simulation)]]
## Stochastic Processes
- [[Arithmetic Random Walk]]
- [[Geometric Random Walk]]
- [[Mean Reversion Process (Ornstein-Uhlenbeck)]]
- [[Jump Process]]
## Risk Pricing & Benchmarking Risk
- [[Risk Valuation]]
- [[RAROC]]
- [[Sharpe Ratio]]
- [[Risk Benchmark]]
	- [[Markowitz Model]] 
	- [[Sharpe CAPM]] - assumes risk is proportional to company value
	- [[Lintner CAPM]] - alternative to CAPM, provides a unique risk measure. Risk charges go in cashflows
	- [[Black-Litterman]] 
## Excel
- [[Loans Amortization]]
- Important Excel Based Modeling
	- Loss given default in excel
		- `IF(rand()<0.05, default, no default)`


## Post Midterm
### Capital Structure 
- Financing structure
- Preferred stock
	- Works more like debt -> pays a perpetual fixed coupon
		- Company can suspend the dividend when they need cash, but there is an accrual feature where they'd pay it back
	- Convertible preferred -> preferred stock converts into equity by a ratio
	- Callable preferrable -> sets a max time to when you can convert
- Equity paid last
- Other funding
	- crowdfunding
	- vendor finance -> seller extends debt to you

- Pro formas
	- Making fabricated scenarios to simulate cash flows
- Claims
	- analyze how the cash falls on capital stack
- Depreciation
	- In commodities, there is an extra term called evaporation (works same way as depreciation/amort) but for commodities expiring
- Dividends vs share buybacks
	- Dividends are taxable events and compulsory
	- Buybacks -> you can choose to participate
		- You create a capital gain -> economists argue this is better because you are buying out the shareholders who value you the least
		- Negative -> there may be better use for cash
- P/E ratio is a special case of [[Lintner CAPM]]
	- One price is a linear function of another
		- $P_2 = \frac{P}{E}_1 * E_2$
		- $V_1 = \mu_1 - A \sigma_1$
		- $V_2 = \mu_2 - A \sigma_2$
			- Set A as equality
- Balance sheet -> view it as a mirror
	- Economic balance sheet
		- Max(Equity + Debt) = Min(assets - other liabilities)
			- Essentially trying to push other liabilities into debt and equity
- Proper risk management adds shareholder value -> by becoming less risky you are granted more debt at a lower rate and this balances up
- Merton Model for capital structure
	- Think of equity as a call option on the assets of a firm
	- 
### Capital Budgeting
- Investment strategy
- Real options
- Project interactions
	- Value this by looking at projects as a portfolio -> will reflect dependencies
	- For a single project - compare portfolio with and without the project
- Discount rates
	- Discount rates are not homogenous
		- Can go through an income statement and assign a different discount rate to each peice (revenue would be the highest)
### Risk Management
- Investment of risk capital (in [[Risk Valuation]])
	- Which risks to take and not to take
- 




**MIdterm**
Pros and cons of using implied probability (midterm)
- Con: its showing risk neutral probabilities not actual ones
last Q
- 
