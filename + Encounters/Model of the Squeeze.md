up:: [[Oil Markets MOC]]
tags:: #Finance
# Stylized Model for the Squeeze
- Builds on [[Canonical Theory of Storage]]
	- 2 bounds: 
		- running out of oil -> spot price will move higher until demand or supply adjust -> unreachable max
		- running out of storage -> spot price will drop to prevent further inflows -> unreachable min
	- Problem: very hard to gauge supply and demand in real life
		- Traders often model inventory instead
- Concept: we model the uncertainty behind the flow of inventories using a [[Mean Reversion Process (Ornstein-Uhlenbeck)]]
	- Reminder: OU process = $dx = k(\bar{x} - x) dt + \sigma dz$
		- $\bar{x}$ = long run mean
		- $k$ = speed of mean reversion
		- if $x(t) > \bar{x}$, inventories will decrease
		- if $x(t) < \bar{x}$, inventories will rise
		- $dz$ = a normal random variable [[Normal Distribution]]
		- $\sigma$ = magnitude of uncertainty
## Decreasing Normal Probability
- As time to maturity $(T-t)$ decreases, the [[Probability Density Function (PDF)]] becomes smaller and smaller
- This is for stochastic inventories

![[Pasted image 20250105173158.png]]

- this is known as the Dirac delta function
	- $\delta(x_T - x) = \begin{cases} 0, & x_T \neq x, \\ \infty, & x_T = x \end{cases}$
	- Falls to 0 except for a single point where it goes to infinity
## Modeling Spread
- Instead of linking inventory to outright price, traders model the spread between spot (short term futures) and another future
- Defined as
$$s(x,t) = F(t, T_1;x) - F(t,T_2;x)$$
### The Squeeze
- The storage problem is essentially reformulated under 3 constraints and we now model the spread mentioned above
$$\begin{equation} s(x_T, T) = \begin{cases} +\infty, & x_T = X_{\min}, \\ -\infty, & x_T = X_{\max}, \\ -C, & X_{\min} < x_T < X_{\max} \end{cases} = \delta(x_T - X_{\min}) - \delta(x_T - X_{\max}) - C \end{equation}$$
- And the closed form formula is 
$$s(x, t) = p(x, t; X_{\min}, T) - p(x, t; X_{\max}, T) - C$$
- With [[Probability Density Function (PDF)]] closed form:
$$\begin{equation} s(x, t) = \frac{1}{\sqrt{2\pi (T - \hat{t})} \, \sigma} e^{-\frac{(y(t) - X_{\min})^2}{2\sigma^2 (T - \hat{t})}} - \frac{1}{\sqrt{2\pi (T - \hat{t})} \, \sigma} e^{-\frac{(X_{\max} - y(t))^2}{2\sigma^2 (T - \hat{t})}} - C \end{equation}$$
### "Getting Squeezed"
- This refers to holding futures until expiry
	- These are fulfilled by a party with a membership at Cushing, and they often do it on terrible terms
		- No traders hold oil near expiry