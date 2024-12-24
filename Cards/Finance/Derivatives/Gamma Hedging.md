up:: [[Derivatives MOC]]
tags:: #Finance 
# [[Gamma]] Hedging
- Reducing the need to constantly rebalance the portfolio by holding a "Gamma neutral" position, where Gamma is 0
	- $\Gamma = \frac{\partial^2 V}{\partial S^2}=0$
	- Used to reduce the **size of each rehedge** and/or to increase the **time between rehedges**, and thus **reduce costs**
- Minimizes exposure to model error
- In practice, this is done by buying/selling more options (not the underlying)
- This is needed because option portfolio dynamics have [[Convexity]], therefore 2nd order hedging is necessary
- Usually hedged at once with [[Delta Hedging]]

