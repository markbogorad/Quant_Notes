up:: [[Fixed Income MOC]]
tags:: #Finance
# Bootstrapping
- A way of deriving [[Bond Spot Rates]] and the [[Yield Curve]]
- Using government bonds to match maturities with the on the run bond, deriving the spot rate
	- Iteratively solve for spot rates, where you start with the shortest maturity and every maturity after depends on the solution for the one before
## Methods
#### Smooth Function Approach
- Fitting a smooth function to yield curve
- Purpose is to minimize abrupt changes
#### Regression Approach
- Using a regression model to determine best fit for the yield curve
#### Cubic Spline
- fits piecewise cubic polynomials between each set of data points (e.g., known yields at specific maturities) on the yield curve
#### Interpolation
- estimate yields at maturities for which no data is available by connecting known data points
- used to fill in gaps between maturities with observed yields.
#### Maximizing Smoothness
- Maximizing smoothness is a criterion used to obtain a yield curve that is as smooth as possible without abrupt changes. 
- This method minimizes the roughness of the curve by optimizing a smoothness criterion, such as minimizing the second derivative (change in slope) across the curve. 
- Smoothing algorithms (e.g., penalized splines) are employed to find the smoothest possible curve that still fits the observed data well