up:: [[Risk Management MOC]]
tags:: #Finance 
# Basel II 1996
- Came about as a response to Asian financial crisis (late 90s)
### 3 pillar system
- 1) Regulatory capital calculation
	- Same definitions on tier 1 and tier 2
	- Market risk component the same
	- Minimum capital the same still 8%
	- credit risk was made more precise 
	- **[[Operational Risk]] came to be recognized here**
	- Total RWAs are now determined by multiplying capital requirements for [[Market Risk]] and [[Operational Risk]] by 12.5 (reciprocal of 8%)
- 2) Capital adequacy - ICAAP adequacy process
	- Will the bare minimum actually protect companies - how much is truthfully needed
- 3) Transparency - market disclosure
	- what information is disclosed to public - how to optimize this 
	- Implemented semi-annual and quarterly disclosures for key components (ex: quarterly tier 1 ratio disclosure)
### Key changes
- Standardized credit risk approach
- Internal ratings based approach revamped ([[Credit Risk]]): **foundation model and advanced model**

| Data Input                   | Foundation IRB         | Advanced IRB     |     |
| ---------------------------- | ---------------------- | ---------------- | --- |
| **PD**                       | Provided by bank       | Provided by bank |     |
| **LGD**                      | Provided by supervisor | Provided by bank |     |
| **Exposure @ Default (EAD)** | Provided by supervisor | Provided by bank |     |
| **Maturity (M)**             | Provided by supervisor | Provided by bank |     |

- **LGD vs EAD**
	- EAD is how much you have outstanding at default - how much money is out there as a risky loan
		- Hard to manage for revolving loans like credit card debt - simulation - large MC engine
		- Maturities for revolving debt is stochastic
	- LGD - accounts for how much people will pay you back - % number of how much you get back incorporating collateral
- [[Operational Risk]] treatment - very simple risk * prob
	- Tried to model this more intensively
		- Actuarial models work better if company doesn't have advanced insight into these events
		- If they do and have enough observations, they can use non parametric models and fit the tails properly
			- Most went to standardized approach because of this
	- 3 methods for OP risk
		- **Basic Indicator Approach** - based on annual revenue of the Financial Institution
		- **Standardized Approach** - based on annual revenue of each of the broad business lines of the Financial Institution
		- **Advanced Measurement Approaches** - based on the internally developed risk measurement framework of the bank adhering to the standards prescribed (methods include IMA, LDA, Scenario-based, Scorecard etc.)
- Market risk 
	- added securitized products
	- IDRC - incremental default risk charge
- Basel II formula
## Capital Ratio
$$\frac{\text{Total Capital}}{\text{Credit RWAs + Market RWAs + OpRisk + IDRC + Securitization Framework}}$$
