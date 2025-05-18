up:: [[Fixed Income MOC]]
tags:: #Finance 
# BEY
- Yield that equates discounted value of the bond to the actual future cashflows
- No closed form formula/solution, uses [[Newton-Raphson Root Search]]
- Useful for comparing bonds of different payment frequencies and different markets
$$y_{i+1}=y_i+\frac{Price_i-Price_{actual}}{Duration_{Dollar}}$$