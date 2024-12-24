up:: [[Quantitative Valuation MOC]]
tags:: #Finance  
# GVE
- Assumes risk free term structure is known (feasible as bonds are available)
- For first half of course, risk is assumed to be reflected via a discount rate or the cash flows were assumed to be guaranteed (risk free)

**Level 1**
$$\text{Required Return} \geq \leq \text{Expected Return}$$
- Seller ($\geq$) expects future returns to equal or fall short of requirements
- Buyer ($\leq$) is expecting return to meet or exceed person requirements

**Level 2**
$$\text{Time Value} + \text{Risk Compensation} = \text{Expected Capital Gain} + \text{Expected Cash Flow}$$
$$rV_0 + k\sigma = \mathbb{E}[V_1] - V_0 + \mathbb{E}[C_1]$$
- Time value (interest earned)
	- A variable capturing [[Opportunity Cost (Valuation)]]
	- $r$ constant risk free rate
	- $V_0$: value of asset today
	- $rV$ is always 0 except for froward and futures (no cash investment required)
- Risk compensation (per period)
	- $\sigma$: risk measure per period
	- $k$: compensation per unit risk
- Expected cash flow
	- $\mathbb{E}[C_1]$: expected cash flow in 1 period
	- **Expected cash flow is usually the first term of the given sequence**
- Expected capital gain ($\Delta$ price)
	- $V_0$: value of asset today
		- $= PV[C_1, C_2, C_3, ...]$
	- $V_1$: value just after $C_1$ is paid
		- $= PV[C_2, C_3, C_4, ...]$
	- $E[V_1] - V_0$
		- Expected capital gain (expectation of future value - value today)
## GVE Features and Assumptions
- Assumes constant interest rate
- Can value private and public assets
- Reconciles differences between buy and sell side
- Can value correlated cash flows (inter temporal correlations, i.e. past correlations influencing future)
- Can incorporate stochastic features



### GVE: Fibonacci Sequence

### GVE: CAPM
### GVE: Single Risky Cash Flow
### GVE: Correlated Cash Flows
- $\Sigma_i$ is variance of portfolio at time $i$ (grand sum of the matrix)
- Key: calculating risk from one period to the next
	- Matrix -> unconditional covariance
		- Ex: 
			- $A = \begin{pmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{pmatrix}$
				- do $a_{22} - (\frac{a_{12} * a_{21}}{a_{11}})$ = $\Sigma_1$ 
					- ...
### GVE: Forward
### GVE: Black-Scholes
### GVE: Normally Distributed Cash Flows
### GVE: Arithmetic Random Walk