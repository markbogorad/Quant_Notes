up:: [[Oil Markets MOC]]
tags:: #Finance
# Hedging Equilibrium
- **Concept:** there is a distinction between the fundamental analysis equilibrium ([[Canonical Theory of Storage]]) and the financial equilibrium (financial vs physical traders)
	- Driven by aggregate demand for hedging services
#### The Theory of Hedging Pressure
- It is difficult to draw a line between speculative investments and hedges at face value
	- Hedges may have internal biases on company board
	- Speculative positions may be rebalancing a portfolio
- The study of interaction between hedgers and speculators is *the theory of hedging pressure*
## Producer vs Consumer Oil Demand
- Propensity (willingness) to hedge is uneven in practice
	- There are more hedgers in the market, and price risks are also higher for producers
- This suggests that the structure of futures prices should naturally be uneven, in particular, that of the [[Theory of Normal Backwardation]]
	- $RP = E_t(S(T)) - F(t,T) > 0$
		- Risk premium
## 3 Party Optimization Problem
- Variables
	- Q = barrels of oil
	- W = wealth
	- $\bar{S}$ = spot price of oil
	- N = number of units traded
	- $\alpha$ = risk aversion coefficient
- Producer optimal position
$$N_p = -Q_p + \frac{E(\bar{S})-F}{\alpha_p*\sigma^2(\bar{S})}$$
- Consumer net wealth
$$\bar{W}_c=-Q_c\bar{P}+(\bar{S}-F)N_c+U_c$$
- Consumer optimal hedge (beta measurement)
$$\beta_c=\rho_{p,s}\frac{\sigma(\bar{P})}{\sigma(\bar{S})}$$
- Speculator optimal position
$$N_s=\frac{E(\bar{S})-F}{\alpha_s \sigma^2(\bar{S})}$$
### Final Equation
$$N_p + N_c + N_s = 0$$
- Futures must be a 0 sum game
- So final risk premium formula:
$$E(\bar{S})-F=\alpha \sigma^2(\bar{S})(Q_p-\beta_C Q_c)$$
- where
$$\alpha = \frac{1}{\frac{1}{\alpha_p}+{\frac{1}{\alpha_c}+{\frac{1}{\alpha_s}}}}$$
	