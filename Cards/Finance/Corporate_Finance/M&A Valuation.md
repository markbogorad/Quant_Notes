up:: [[Corporate Finance MOC]]
tags:: #Finance 
# Valuation
## DCF
- [[Corporate Valuation]]
- Done via the [[WACC]]
	- Measures risk of the firm by accounting for [[Cost of Capital]] of both equity and debt
$$ \begin{equation} WACC = r_e \left( \frac{E}{D + E} \right) + r_d (1 - t) \left( \frac{D}{D + E} \right) \end{equation}$$
- $r_e = \text{proportion of equity in financing}$
- $E = \text{market value of equity}$ 
	- = $\text{Stock Price} \times \text{Number of Shares}$
- $r_d = \text{proportion of debt financing}$
- $D = \text{market value of debt}$ 
	- = $\text{Bond Price} \times \text{Number of Bonds}$
- $t = \text{corporate tax rate}$ 

$$PV = \frac{FCF_1}{(1 + WACC)^1} + \frac{FCF_2}{(1 + WACC)^2} + \cdots + \frac{FCF_T}{(1 + WACC)^T}$$
- Add the terminal value to the final stable cashflow (see [[Corporate Valuation]] when growth is non constant)
## Adjusted Present Value (APV)
- Useful for [[Distress Restructuring]] and [[Leveraged Buyout (LBO)]] as well
- $APV = V_L = V_U + PV(TS)$
	- $V_U$ = unlevered firm (100% equity)
	- $V_L$ = levered firm (100% debt)
	- TS is tax shield
	- Same as Modigliani and Miller proposition with no taxes in [[Capital Structure]]
- 1) Value as if you only use equity financing with forecasted cash flows and [[WACC]]
	- $V_U = \frac{FCF_1}{(1 + r_A)^1} + \frac{FCF_2}{(1 + r_A)^2} + \cdots + \frac{FCF_T}{(1 + r_A)^T}$
- 2) add on the present value of the tax shield of debt

## Multiples Valuation
- See [[Corporate Valuation]] multiples valuation
- ![[Pasted image 20240615153806.png]]

## Value of an Offer
- $P = c N_B + \frac{x N_B}{N_A + x N_B} (V_A + V_B + S - c N_B)$
	- Cash component : $cN_B$
		- Cash (c) per share of target ($N_B$)
	- Equity component: $\frac{x N_B}{N_A + x N_B} (V_A + V_B + S - c N_B)$
		- Subtract the cash paid out in the merger $cN_B$
		- $xN_B$ = number of shares that each share in the target gets (x) times number of share in target
			- Same as number of shares post merger
		- $N_A$ = shares in acquirer
		- $\frac{x N_B}{N_A + x N_B}$ is the proportion of shares in the post-merger company that will be owned by the target