up:: [[Oil Markets MOC]]
tags:: #Finance 
# Time Dependent Local Volatility
- When you have time-dependent volatility, the effective volatility used for option pricing simplifies to the quadratic (root mean square) average of local volatility over time.
- Implied vol is quadratic average of local vols
	- **Just average the vol quadratically and plug it into the BS equation to get your price**
- [[Black-Scholes]]
	- $\nu = \sqrt{\frac{1}{T_0 - t} \int_t^{T_0} \sigma_G^2(s, T) \, ds}$
- [[Bachelier Option Model]]
	- $\nu_N = \sqrt{\frac{1}{T_0 - t} \int_t^{T_0} \sigma_A^2(s, T) \, ds}$
- Continuous (integrated)
$$\nu^2(T) = \frac{1}{T} \int_0^T \sigma_G^2(\tau) \, d\tau$$
- Conclusion is variance is additive
![[Pasted image 20250309160951.png]]
- 23 is average between 17 and 30 in quadratic sense
- Local is always steeper
- Local determines the process
- Volatility decrease exponentially through time
$$\sigma_G(\tau) = \sigma_\infty + \sigma_0 e^{-k\tau}$$
- Implied vol formula
$$\nu(T) = \sqrt{ \sigma_\infty^2 + 2\sigma_\infty \sigma_0 \frac{1 - e^{-kT}}{kT} + \sigma_0^2 \frac{1 - e^{-2kT}}{2kT} }$$
## Reconstructing the Local Vol Process in Time
Practial example; [[Local Volatility Bootstrapping]]
- Back out local volatility from implied volatility using time homogenous vol (vol only depends on time)
- Differentiate with respect to upper limit using quadratic average formula: $\nu^2(T) = \frac{1}{T} \int_0^T \sigma^2(\tau) \, d\tau$
$$\sigma^2(T) = \frac{\partial}{\partial T}\left[T \cdot \nu^2(T)\right]$$
- No arbitrage condition by: $\frac{\partial}{\partial T}\left[T \cdot \nu^2(T)\right] \geq 0$ (means no negative variance)
- ![[Pasted image 20250309162338.png]]

