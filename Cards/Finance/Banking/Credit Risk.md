up:: [[Risk Management MOC]]
tags:: #Finance 
# Credit Risk
- *Risk that a bank borrower or counterparty will fail to meet its obligations in accordance with agreed terms or their creditworthiness will deteriorate*
	- Encompasses 
		- [[Counterparty Credit Risk]] 
		- [[Credit Valuation Adjustment (CVA)]]
		- Lending Risk 
- Pricing Credit Instruments
	- Price the portfolio as if it would have been tradable asset
- Important concept: who is my credit risk to?
	- Answer: whoever you end up suing
	- Issuers - physical name on the contract
	- Guarantor - municipality 
	- Obligor - the person legally obligated to pay
- Bond credit risk
	- Issued by agents + additional guarantee from local govt
- 3 main pieces
	- Lending (Conventional credit risk from loans)
	- Bonds (issuer risk) 
		- For bond or loan
		- Risk that issuer of debt securities will default 
	- [[CVA]]
		- For derivative transactions, repos, structured products
- Does capital cover expected or unexpected credit losses?
	- Unexpected (expected losses are covered via regular lending rates)
![[Screenshot 2025-05-12 at 9.27.22 AM.png]]
## Mitigation Techniques
- Netting agreements
- Posting of collateral
- Diversification
## Credit Risk Drivers
- Probability of default (hazard rates)
	- Uses a bunch of logistic regression models (a structural model)
	- [[Vasicek Interest Rate Model]]
		- Applicable for a huge portfolio of loans so diverse that its ok to average (artificial setup where number of borrowers go to infinity and loans are homogenous)
- Loss given default (1-r)
- Exposure at default
## Modeling credit risk
- Modeling recoveries ([[Structural Models for Default]])
- Modeling counterparties ([[CVA]])
- Controlling prescriptions by regulators (modeling RWAs)
	- EEPE Effective Expected Positive Exposure
		- Regulator requirement for banks to be more conservative about their exposure
	- Theres also a CVA add on here thats a VaR style sensitivity computation
- Internal models approach
	- Uses internal ratings to reflect knowledge on counterparty
- IRB approach - taking prescriptions from internal models 
## Recovery rates
- Fluctuate around 40% for corporate bonds (very different across credit instruments)
## Securitization Framework
- A response from regulators to the events of 2008
- Securitization is any kind of loan packaging 
	- Issue bonds on behalf of the pool
	- Tranche the bonds
	- AAA -> low coupon, low interest, low default
	- BBB -> high coupon, high prepay, high default
---
### Bayes Content
- Expected risk is covered with **loan loss provision**
- Unexpected losses are covered with [[Bank Capital]]
- Credit risk is managed via **diversification**
	- Reduces idiosyncratic (stock specific) risk
	- Still have systematic risk (recessions)
- Credit risk is commonly reflected in corporate bonds via the [[Credit Spreads (Hazard Rates)]]
- Stems from the information asymmetry issue in banking ([[Asset Transformation Function]]) with regards to risk
	- Borrower can go rogue
## Origin of Credit Risk
**3 Dimensions:**
1) **Risk:** banks claim against borrowers is riskier than the depositors claim against the bank
2) **Maturity:** assets have longer maturities than liabilities
3) **Liquidity:** Assets have lower liquidity than liabilities
## Bank Loans
- Most common types and their frequency
- C&I -> commercial and industrial
- Most loans are collateralized

|             | Amount ($ millions) | Percent (%) |
|-------------|----------------------|-------------|
| **Total loans*** | $6,739.8             | 100.0%      |
| **C&I**           | 1,322.1              | 19.6%       |
| **Real estate**   | 3,562.3              | 52.9%       |
| **Individual**    | 1,183.0              | 17.5%       |
| **Other**         | 672.4                | 10.0%       |

- **Non performing loan:** 90 days past due
## Mitigating Credit Risk
- Screening borrowers
- Collateralize contracts
- Measure risks and establish limits

**Removal Strategies** 
- Loan sales
- [[Securitization]]
- [[Derivatives MOC]]: creates [[Off Balance Sheet Risk]] 
## Credit Ratings
- Agencies are in theory unbiased
- Companies have an incentive to shop around for whichever credit agency gives them the best rating
	- Agencies know they are competing for these customers, and might be complaint with each other, irrationally raising credit ratings
### What Standard Default Rates Look Like:
![[Pasted image 20240516141319.png]]

## Portfolio Credit Risk
- Asymmetric and leptokurtic (higher peak and fatter tails) [[Sample Moments Glossary]]
- Uses credit value at risk [[CVaR]]
- Main models:
 ![[Pasted image 20240516152604.png]]
## Credit Risk vs [[Market Risk]]

| Category                             | Market Risk                                                                 | Credit Risk                                                                |
|--------------------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------|
| **Liquidity**                        | Liquid markets (except crisis/small stocks)                                 | Illiquid markets (except some credit derivatives, securitization...)      |
| **Data**                             | Available, long, continuous                                                 | Proprietary, short, infrequent                                             |
| **Risk Measurement and Pricing**     | Well developed (VaR, ES, Stressed-VaR, CAPM, APT)                           | Undeveloped. Some tools, not always applicable, mainly based on rating (with limitations) |
| **Hedging Instruments**              | Wide range of exchange-traded/OTC derivatives                                | Limited range of credit derivatives, wide spreads                         |
| **Information and Institutional Problems** | Market abuse/manipulation/collusion (on several recent cases)               | Severe, especially retail credit and high-yield bonds                     |
| **Risks**                            | Well understood (non-normal)                                                | Very different depending on the borrower. Not well-understood              |
| **Trading Strategies**               | Active short-term trading                                                   | Mostly held on buy/hold                                                    |

