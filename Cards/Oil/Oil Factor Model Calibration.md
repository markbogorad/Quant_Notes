up:: [[Oil Markets MOC]]
tags:: #Finance 
# Calibration
- Fitting the [[Two Factor Stochastic Convenience Yield Model (Oil)]]
- Calibration is the process of finding the **model parameters** that best reproduce **market data**. For this model, the goal is to find values for the parameters $μ,ky,yˉ,σ1,σ2,ρ$ that make the model-generated futures prices match the observed futures prices as closely as possible.
	- This method basically introduces a time dependent [[Convenience Yield]] to ensure consistency with empirical futures
		- Similar to [[Hull-White Model]]
		- Initial convenience yield: $y_0(T) = r - \frac{\partial \ln(F(0, T))}{\partial T}$
		- Time dependent yield: $\bar{y}(t) = \frac{1}{k_y} \frac{\partial y_0(t)}{\partial t} + y_0(t) + \frac{\sigma_2^2}{2k_y^2}(1 - e^{-2k_yt}) - \frac{\rho \sigma_1 \sigma_2}{k_y}$
## Challenges
- **Market Data is Noisy**: Futures prices can be affected by short-term supply shocks, geopolitical factors, etc. Will have unstable [[Implied Volatility]]]
- **Interdependence of Parameters**: The parameters are not independent of each other, making it hard to isolate them for estimation.
- **Complexity of the Analytical Solution**: The model solution involves solving ordinary differential equation for A(τ) and B(τ), which complicates calibration.