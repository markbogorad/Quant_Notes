up:: [[Oil Markets MOC]]
tags:: #Finance 
# Two Factor Stochastic Convenience Yields
- **S(t) (spot price)** is stochastic and is influenced by the current [[Convenience Yield]] y(t).
- **y(t) (convenience yield)** mean-reverts to its long-term average $\bar{y}$​ at speed ky​.
- The correlation ρ captures the relationship between fluctuations in the spot price and changes in the convenience yield.
- This model is more realistic because it accounts for inventory-driven pricing dynamics and the variability of convenience yields.
## Two Stochastic Processes
$$\frac{dS}{S} = (r - y) dt + \sigma_1 dZ_1$$
$$dy = k_y (\bar{y} - y) dt + \sigma_2 dZ_2$$
- Where:
	- S(t) = Spot price
	- y(t) = Convenience yield
	- r = Risk-free rate
	- $\bar{y}$​ = Long-term mean of the convenience yield
	- ky​ = Speed of mean reversion for y(t)
	- $σ_1,σ_2$​ = Volatilities of the spot price and convenience yield, respectively
	- $dZ_1​$ and $dZ_2$​ are **correlated Brownian motions** with correlation ρ: $dZ_1dZ_2=\rho dt$
## Key Benefits
- **Futures Curve Shapes**: This model allows for more complex shapes (humped, contango, backwardation) due to the interaction between the spot price and stochastic convenience yield.
- **Volatility Structure**: Unlike the one-factor models, volatility does not decay to zero with increasing maturity.
- **Mean Reversion**: Indirect mean reversion in prices is induced by the mean-reverting convenience yield process.