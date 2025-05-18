up:: [[Oil Markets MOC]]
tags:: #Finance 
# One Factor Mean Reverting (Schwartz 1997)
- Assumes log spot price (NOT log returns) follow a [[Mean Reversion Process (Ornstein-Uhlenbeck)]]
- $dX = k(\alpha - X) dt + \sigma dZ$
- Important feature: captures volatility decay (Saumelson effect)
	- $\sigma_F(\tau) = \sigma e^{-k\tau}$
## Derivation of PDE
- Risk neutral process
	- $dS = k(\mu - \ln(S) - \lambda \sigma) dt + \sigma S dZ$
		- Lambda is the market price of risk
- [[Ito's Lemma]]
	- $\frac{\partial F}{\partial t} + \frac{\sigma^2 S^2}{2} \frac{\partial^2 F}{\partial S^2} + k(\mu - \ln(S) - \lambda \sigma) S \frac{\partial F}{\partial S} = 0$
- Solution
	- $\ln(F(S, \tau)) = e^{-k\tau} \ln(S) + (1 - e^{-k\tau})(\alpha - \lambda \sigma) + \frac{\sigma^2}{4k}(1 - e^{-2k\tau})$
## Pros
- **Mean Reversion**: Prevents prices from drifting too far from a long-term mean, which is more realistic for commodities like oil.
- **Volatility Decay**: Short-term volatility is higher, but it decays over time to a stable long-term level.
- **More Realistic Futures Curves**: The model allows for futures prices that flatten as maturity increases, matching real-world data better than the log-normal model.


