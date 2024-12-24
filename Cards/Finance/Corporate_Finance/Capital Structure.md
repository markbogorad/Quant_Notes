up:: [[Corporate Finance MOC]]
tags:: #Finance 
# Capital Structure
- Proportion of debt and equity that compose your comapny
**Dynamics:**
	![[Pasted image 20240615123958.png]]

## Models for Ideal Capital Structure
**Modigliani and Miller no Taxes**
- Depends on [[Market Efficiency]], if market is efficient there should be no difference between debt and equity
- $V_U = V_L (= E_L + D_L)$
	- $V_U$ = unlevered firm (100% equity)
	- $V_L$ = levered firm (100% debt)
	- $(E_L+D_L)$ = equity of levered firm + debt of levered firm

**Modigliani and Miller with Taxes**
- Accounts for a tax shield with debt
	- $\text{PV(Tax Shield)} = \frac{t r_D D}{1 + r_D} + \frac{t r_D D}{(1 + r_D)^2} + \cdots = \frac{t r_D D}{r_D} = t D$
		- $tr_D D$ is the tax shield for any given period where D is the debt and $r_D$ is the interest on debt
- MM with taxes = ${V_L = V_U + tD}$

| **Aspect**                    | **MM without taxes**   | **MM with taxes**      |
| ----------------------------- | ---------------------- | ---------------------- |
| **Firm value**                | unchanged              | increase with leverage |
| **Cost of equity**            | increase with leverage | increase with leverage |
| **WACC**                      | unchanged              | decrease with leverage |
| **Optimal capital structure** | none                   | 100% debt              |



**Trade-off Theory**
- Assume taxes and bankruptcy costs
- More debt will cause higher interest payments and more stress on company
- $V_L = V_U + \text{PV(Tax Shield)} - \text{PV(Costs of Financial Distress)}$
	- Firms with low expected distress should load up on debt
	- Costs of distress = probability of distress * cost of distress 

**Default Risk Methods**
- Help find optimal structure depending on default conditions
- [[Scoring Models]] - Altmans Z score used
- Mertons Model
	- $\text{Risk-neutral default prob}_{(0,T)} = 1 - e^{-\text{credit spread} \times T / (1 - R)}$
- [[WACC]] method
	- Find debt-equity ratio that maximizes EBIT
		- Uses Hamadas equation [[Cost of Capital]]
	- similar to [[Optimization]]
	- Do WACC at different ratios (trial and error) to find ideal
		- ![[Pasted image 20240615130133.png]]
	