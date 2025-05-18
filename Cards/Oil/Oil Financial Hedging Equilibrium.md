up:: [[Oil Markets MOC]]
tags:: #Finance
# Hedging Equilibrium
- Essence of the theory of hedging pressure [[Flow Oil Theory (Hedging Pressure)]]
-  **Concept:** there is a distinction between the fundamental analysis equilibrium ([[Canonical Theory of Storage]]) and the financial equilibrium (financial vs physical traders)
	- Driven by aggregate demand for hedging services
	- Speculative demand can outweigh traditional supply demand dynamics
	- Arbitrage often comes from **hedging imbalances**
		- Ex: [[Strategic Petroleum Reserve (SPR)]] case study where govt had to hedge, 
		- Ex: scenarios where someone can't access market like airlines, etc - this is where most make money
- This essentially maps out the objectives of the key parties involved in oil trading
	- **Producers** (hedgers)
	- **Consumers**
	- **Speculators** (no endowment, liability, or hedging mandate) 
	- **Inflation Hedgers** - [[Presence of Inflation Hedgers]] (Bridgewater)
#### The Theory of Hedging Pressure
- It is difficult to draw a line between speculative investments and hedges at face value
	- Hedges may have internal biases on company board
	- Speculative positions may be rebalancing a portfolio
- The study of interaction between hedgers and speculators is *the theory of hedging pressure* and the root of [[Flow Oil Theory (Hedging Pressure)]]
- Propensity (willingness) to hedge is uneven in practice
	- There are **more hedgers in the market**, and price risks are also higher for producers
- This suggests that the structure of futures prices should naturally be uneven, in particular, that of the [[Theory of Normal Backwardation]]
	- $RP = E_t(S(T)) - F(t,T) > 0$
		- Risk premium
## Optimal Hedging Problem
- Variables
	- P = Producer (hedger)
	- C =  Consumer
	- S = Speculator
	- I = Inflation Hedger
	- Q = barrels of oil
	- W = wealth
	- $\bar{S}$ = spot price of oil
	- N = number of units traded
	- $\alpha$ = risk aversion coefficient
### Assume a Mean-Variance Framework
- All participants are risk averse
- Each try to maximize their own wealth with quadratic utility function: 
 $$\max \left\{ \mathbb{E}(\tilde{W}) - \frac{\alpha}{2} \text{Var}(\tilde{W}) \right\}$$
### Producer Optimal Position
- The producer has an initial endowment of $Q_p$​ oil barrels and incurs a fixed cost $U_p$​.
- To hedge price risk, the producer trades $N_p$​ futures contracts at price $F$.
- The futures price will eventually converge to the spot price $\bar{S}$ in the next period.
- Initial setup:
	- Expected wealth: $\mathbb{E}(\tilde{W}_p) = Q_p \mathbb{E}(\tilde{S}) + N_p (\mathbb{E}(\tilde{S}) - F) - U_p$
	- Expected variance: $\sigma^2(\tilde{W}_p) = (Q_p + N_p)^2 \sigma^2(\tilde{S})$
- First order condition:
	- $\mathbb{E}(\tilde{S}) - F - \alpha_p (Q_p + N_p) \sigma^2(\tilde{S}) = 0$
- Optimal position:
$$N_p = -Q_p + \frac{E(\bar{S})-F}{\alpha_p*\sigma^2(\bar{S})}$$
- Negative barrels to hedge (Q) + a term to adjust your view (hedging less if futures are cheap and etc. depending on risk aversion)
### Consumer Optimal Position
 - Most consumers consume refined products
	- Exposes them to [[Basis Risk]] from cross hedging -> captured by Beta here
$$\bar{W}_c=-Q_c\bar{P}+(\bar{S}-F)N_c+U_c$$
- Negative endowment to hedge + transactions in futures + revenue from business
	- P = price of refined product, S is the price of futures
	- Since it's a refined product, you have a proxy hedge (Cross Hedge)
- Consumer optimal hedge (beta measurement)
$$N_C=\beta_c Q_c+\frac{E(\bar{S})-F}{a_c\sigma(\bar{S})}$$
- Where beta is a measure used to reduce or increase sensitivity of a specific commodity to crude oil (reminder: working with refined products on consumer side)
	- Very important ex: if you're an airline and you hedge jet fuel by buying WTI futures, 2020 would have messed you up because WTI went negative and jet fuel did nothing
$$\beta_c=\rho_{p,s}\frac{\sigma(\bar{P})}{\sigma(\bar{S})}$$
- Speculator optimal position

### Speculator Optimal Position
$$N_s=\frac{E(\bar{S})-F}{\alpha_s \sigma^2(\bar{S})}$$
- Same as producer just no prior endowment
### Inflation Hedger Optimal Position
- [[Presence of Inflation Hedgers]]
- Same as speculator just beta is now specific for inflation
$$N_i=\beta_i Q_i+\frac{E(\bar{S})-F}{a_i\sigma(\bar{S})}$$
## Hedging Pressure Equilibrium
- Positions summary:
$$N_p + N_c + N_i + N_s = 0$$
	- $N_p = -Q_p + \frac{\mathbb{E}(\tilde{S}) - F}{\alpha_p \sigma^2(\tilde{S})}$
	- $N_c = \beta_c Q_c + \frac{\mathbb{E}(\tilde{S}) - F}{\alpha_c \sigma^2(\tilde{S})}$
	- $N_i = \beta_i Q_i + \frac{\mathbb{E}(\tilde{S}) - F}{\alpha_i \sigma^2(\tilde{S})}$
	- $N_s = \frac{\mathbb{E}(\tilde{S}) - F}{\alpha_s \sigma^2(\tilde{S})}$
- Algebraically, the equilibrium equation becomes
$$Q_p - \beta_c Q_c - \beta_i Q_i = \frac{\mathbb{E}(\tilde{S}) - F}{\sigma^2(\tilde{S})} \left( \frac{1}{\alpha_p} + \frac{1}{\alpha_c} + \frac{1}{\alpha_i} + \frac{1}{\alpha_s} \right)$$
	- Risk premium is
$$\mathbb{E}(\tilde{S}) - F = \alpha \sigma^2(\tilde{S}) (Q_p - \beta_c Q_c - \beta_i Q_i)$$
	- Where $\alpha = \frac{1}{\frac{1}{\alpha_p} + \frac{1}{\alpha_c} + \frac{1}{\alpha_i} + \frac{1}{\alpha_s}}$
	