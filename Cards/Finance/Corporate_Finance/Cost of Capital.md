up:: [[Corporate Finance MOC]]
tags:: #Finance 
# Cost of Capital
- The minimum rate of return from the company's profits that will satisfy the shareholders 
- This is calculated by averaging the company's **equity** and **debt**, forming the [[WACC]]
## Cost of Equity
- Return on investment for equity holders
### Dividend Discount Model
$$ r_e = \frac{D_1}{P_0} + g $$
Where
- P0 = stock price at time 0 (now)
- D1 = dividend at time 1 (next period)
- G = growth rate
- Re = cost of equity
### Earnings Cap Model
$$ r_e = \frac{EPS_1}{P_0} $$
- Projected earnings next year / current stock price per share
### CAPM
- see [[CAPM]] for more info on Portfolio Theory side
$$E(R_i) = R_f + \beta_i \times [E(R_m) - R_f] $$
- Rm-Rf is the **market risk premium**
- Rf is typically proxied by 10 year STRIPS or treasury bonds
- Rm is typically proxied by SP500
#### Beta
- Calculating: $\frac{\text {covariance of stock and market}}{\text {variance of market}}$
	- = $\frac{\rho_{sm} \times \sigma_s^2}{\sigma_m^2}$
		- where:
			- $ρ_{sm}$​ is the correlation coefficient between the stock and the market.
			- $σ_s^2$​ is the variance of stock returns.
			- $σ_m^2​$ is the variance of market returns.
- Unlevering (Hamada's Equation)
	- $\beta_\text{Equity} = \beta_\text{Unlevered} \left( 1 + (1 - t) \frac{\text{Debt}}{\text{Equity}} \right)$ or $\frac{\text{Unlevered Beta}}{\frac{1-Cash}{Firm Value}}$
	- Separates financial and business risks, where financial risk is measured by levered beta
		- Essentially removed [[Capital Structure]] to get unlevered beta (raw beta)
	- Levered beta should be greater than unlevered
## Cost of Debt
- Return on investment for debt providers (banks)
### Yield to Maturity Model
- Used when debt is publicly traded (from [[Fixed Income MOC]])
- $PV = C \times \left( \frac{1}{r} \right) \times \left[ 1 - \frac{1}{(1 + r)^T} \right] + \frac{F}{(1 + r)^T}$
	- Where YTM is $\frac{C + F}{(1 + YTM)^T}$
	- After-tax cost of debt = $YTM \times (1 - \text {Tax Rate})$
### Rating and Default Premium
- If debt is not publicly traded
- Risk free rate + default premium
	- Default premium = credit rating of debt * 0.01
### Debt Beta and CAPM
- $Er_d = r_f + \beta_d \times (\mathbb{E}[R_\text{Mkt}] - r_f)$
	- Incorporates a default factor
### Unrated Debt
- Analysts estimate a synthetic rating from comparable firms, use ratio analysis, or examine recent borrowing history

**These form the [[WACC]]**
