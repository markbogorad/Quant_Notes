up:: [[Fixed Income MOC]]
tags:: #Finance
# Key Rate Duration
- Measures [[Duration Model]] at specific points in the yield curve [[Yield Curve]]
	- Specific points on the curve are "key rates"
	- Allows for measuring sensitivity when shifts are [[Non-Parallel Shifts in the Yield Curve]]
		- One piece might shift more than another -> duration does not pick this up
- Key rate duration measures bond price sensitivity to a 1% change in yield
## KRD Formulae:
- If rates increase
	- $\text{KRD} = \frac{P_0 - P_+}{\Delta y P_0}$
		- Bond price increase / % change in YTM * initial price
- If rates decrease
	- $\text{KRD} = \frac{P_- - P_0}{\Delta y P_0}$
		- Bond price decrease / % change in YTM * initial price
- Ex: key rate duration of 2
	- A bond price is expected to change by 2 when there is a 1% change in yield
### Alternatively, using differentials
- [[Calculus MOC]]
- $D_K = -\frac{1}{P} \cdot \frac{\partial P}{\partial y_K}$
	- $P$ is the bond's current price. 
	- ${\partial P}$ is the change in the bond's price. 
	- ${\partial y_K}$ is the change in the yield for the specific key rate $(K)$.
		- K is the specific point on the yield curve and y is that change
## Change in Bond Price for Portfolio
$$ \Delta \text{Bond Price} = -1\sum_{i=1}^{n} D_{K_i} \cdot \Delta y_{K_i}$$
- The change in the bond price is the sum of all key are durations (at their specific points in time) * the change in yield for that specific period