up:: [[Fixed Income MOC]]
tags:: #Finance
# SEDUR
- Short End Duration
	- Measures bond price sensitivity to changes in short term interest rates (1 year or less)
- $\text{SEDUR} = -\frac{1}{P} \cdot \frac{\partial P}{\partial y_{\text{short}}}$      OR      $\text{SEDUR} = \frac{P_s - P_f}{2 P_0 \Delta y}$
	- (Price in steepening - price in flattening) / 2 * change in yield (in bps) * price at T0
		- [[Non-Parallel Shifts in the Yield Curve]]
		- Price in steepening = original interest rate - change in bps
		- Price in flattening = original interest rate + change in bps
- Short term bond price change:
$$\text{Price Change}_{\text{short}}\approx \text{-SEDUR} \times \Delta y_{short} \times P$$
# LEDUR
- Long end duration
	- Measures bond price sensitivity to changes in long term interest rates (10 years+)
- $\text{LEDUR} = -\frac{1}{P} \cdot \frac{\partial P}{\partial y_{\text{long}}}$      OR    $\text{LEDUR} = \frac{P_f - P_s}{2 P_0 \Delta y}$
	- (Price in flattening - price in steepening) / 2 * change in yield (in bps) * price at T0
- Long term bond price change:
	$$\text{Price Change}_{\text{long}}\approx \text{-LEDUR} \times \Delta y_{long} \times P$$
