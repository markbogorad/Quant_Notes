up:: [[C++ MOC]]
tags:: #Programming
# Exact Solutions C++
## Uses:
- Price options with dividends
- Price indexes, futures, currencies
- Determining accuracy of other methods (as a 2nd check basically)
## One Factor Pricing
- For European Options
- Uses [[Black-Scholes]]
## American Perpetual Options
- Options that go on forever with early exercise features
- There are exact approximations (Barone-Adesi-Whaley) for the early exercise features, but no exact solution
## Affine Models
- Need to model term structure of interest rates here
- Methods:
	- CIR method
		- Beta = 1/2 in SDE
	- Vasicek
		- Beta = 0 in SDE