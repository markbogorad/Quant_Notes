up:: [[Oil Markets MOC]]
tags:: #Finance
# Stylized Model for the Squeeze
- Commodity price is a function of stochastic inventories
	- Price is a financial derivative of stochastic inventories
- The **presence of boundaries** impact decision making today 
	- Dynamic systems 
	- Forces [[Oil Inventories]] to mean revert and inventories to stabilize
		- *If you start seeing low inventories, you won't want to be short due to probability of getting squeezed*
		- *If you see storage is full, you won't want to be long because what if you have to deliver the stuff?*
- Builds on [[Canonical Theory of Storage]] and [[Robinson Crusoe Problem (Oil)]]
	- 2 bounds (infinity squeezes): 
		- running out of oil -> spot price will move higher until demand or supply adjust -> unreachable max
		- running out of storage -> spot price will drop to prevent further inflows -> unreachable min
	- Problem: very hard to gauge supply and demand in real life
		- Traders often model inventory instead
- Concept: we model the uncertainty behind the **flow** of inventories using a [[Mean Reversion Process (Ornstein-Uhlenbeck)]]
	- Captures the balancing mechanism of [[Robinson Crusoe Problem (Oil)]]
	- Reminder: OU process = $dx = k(\bar{x} - x) dt + \sigma dz$
		- $\bar{x}$ = long run mean
		- $k$ = speed of mean reversion
		- if $x(t) > \bar{x}$, inventories will decrease
		- if $x(t) < \bar{x}$, inventories will rise
		- $dz$ = a normal random variable [[Normal Distribution]]
		- $\sigma$ = magnitude of uncertainty
![[Pasted image 20250211155402.png]]
- The gravity induced by the mean reversion pulls us away from the bounds, changing the shape of the curve
	- There is a decreasing normal probability:
![[Pasted image 20250105173158.png]]
- As time to maturity $(T-t)$ decreases, the [[Probability Density Function (PDF)]] becomes taller and has less variance
	- We become increasingly confident that we'll mean revert (this is the gravity)
- Starts to look like the Dirac delta function
	- $\delta(x_T - x) = \begin{cases} 0, & x_T \neq x, \\ \infty, & x_T = x \end{cases}$
	- Falls to 0 except for a single point where it goes to infinity
- **This says that the probability of getting squeezed is increasing with time to maturity**
	- This is also why trading volume is concentrated in front end
## Modeling Spread
$$s(x,t)=p(x,t;X_{min},T)−p(x,t;X_{max},T)−C$$
- $p(x,t;X_{min}​,T)$: Probability of hitting the lower bound (stockout).
- $p(x,t;X_{max},T)$: Probability of hitting the upper bound (tank top).
- C: Cost of storage.
### The Squeeze
- It's called the squeeze because 2 arbitrageurs will get squeezed at the limits, either because of lack of inventories or because of lack of storage
- The storage problem is essentially reformulated under 3 constraints and we now model the spread mentioned above
$$\begin{equation} s(x_T, T) = \begin{cases} +\infty, & x_T = X_{\min}, \\ -\infty, & x_T = X_{\max}, \\ -C, & X_{\min} < x_T < X_{\max} \end{cases} = \delta(x_T - X_{\min}) - \delta(x_T - X_{\max}) - C \end{equation}$$
- And the closed form formula is 
$$s(x, t) = p(x, t; X_{\min}, T) - p(x, t; X_{\max}, T) - C$$
- With [[Probability Density Function (PDF)]] of the difference between 2 Dirac Delta functions
$$\begin{equation} s(x, t) = \frac{1}{\sqrt{2\pi (T - \hat{t})} \, \sigma} e^{-\frac{(y(t) - X_{\min})^2}{2\sigma^2 (T - \hat{t})}} - \frac{1}{\sqrt{2\pi (T - \hat{t})} \, \sigma} e^{-\frac{(X_{\max} - y(t))^2}{2\sigma^2 (T - \hat{t})}} - C \end{equation}$$
