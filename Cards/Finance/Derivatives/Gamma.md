up:: [[Derivatives MOC]]
tags:: #Finance 
# Gamma
>"A measure of by how much or how often a position must be rehedged in order to maintain a delta-neutral position" - Wilmott
$$\Gamma = \frac{\partial^2 V}{\partial S^2} \hspace{1cm} OR \hspace{1cm} \frac{dDelta}{dUnderlying}$$
- **Sensitivity of [[Delta]] to the underlying**
	- Helps understand how stable [[Delta]] is
		- A high gamma would mean [[Delta]] is unstable and hedging strategies will need to be updated more often
- The higher the costs associated with buying or selling the underlying, the higher the Gamma
- All options have positive Gamma
	- You will gain deltas in the direction of the underlying moves (positive for increase in underlying and negative for decrease)
## Gamma Relationships

![[Pasted image 20240629123046.png]] 

![[Pasted image 20240629140404.png]]
- No specific rule for [[Implied Volatility]], lower volatility does not always have higher gamma
- Time to expiry: options near at the money have increased gamma (height of curves)
	- [[Delta]] is more sensitive to changes in underlying as options move closer to expiry

## Cash Gamma
- The amount by which cash delta will move for a 1% change in the underlying
- Gives an indication of position size
- $\text{Deltas per } 1\% = \frac{\text{Cash Gamma}}{\text{Cash Delta}}$ 
	- $\text{Cash Gamma} = \text{Deltas per } 1\% \times \text{Cash Delta}$
- 