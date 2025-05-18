up:: [[Oil Markets MOC]]
tags:: #Finance 
# Reduced Form Stochastic Models
- Reduced-form models are designed to generate **synthetic futures price curves** by modeling key underlying processes:
	- **Spot price dynamics** (S(t)): Typically a log-normal or mean-reverting process.
	- [[Convenience Yield]] dynamics (y(t)): This represents the implicit benefit of holding the physical commodity rather than a futures contract and can also be stochastic.
	- [[Mean Reversion Process (Ornstein-Uhlenbeck)]] For models like **Schwartz (1997)** and **Gibson-Schwartz (1990)**, the spot price or convenience yield follows an Ornstein-Uhlenbeck process, meaning prices are "pulled" back to a long-term equilibrium level.
	- Volatility decay
- One factor models only captures spot price dynamics alone
	- [[One Factor Lognormal Model (Oil)]]
	- [[One Factor Mean-Reverting Model (Oil)]]
- Two factor models capture convenience yield and more
	- [[Two Factor Stochastic Convenience Yield Model (Oil)]]
## General Observations on Oil Behavior in Context of Stochastic Models
- There is mean reversion
	- High price → production increases, consumption declines and oil is supplied from storage
	- Low price → production curtails, consumption rises and demand for storage increase
- Futures curve is driven by 2 factors
	- Long-term price is driven by marginal cost of production ([[Fundamental Oil Theory]])
	- Short-term price is determined as a [[Time (Calendar) Spreads]] to long-term price; the time spread is driven by [[Oil Inventories]]
- Volatility declines with time to maturity (Samuelson effect)
	- Short-term fundamental volatility is high
	- Long-term structural volatility is relatively low
	- Storage buys time for imbalances to normalize which reduces volatility over time
	- The slope of volatility term structure relates to the speed of price mean-reversion (“reduced form” models)