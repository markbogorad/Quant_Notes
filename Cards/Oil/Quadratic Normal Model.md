up:: [[Oil Markets MOC]]
tags:: #Finance 
# Quadratic Normal Model / Local Normal Volatiltiy
- Assume [[Local Volatility]] is quadratic (behaves like a parabola) - [[Bachelier Option Model]]
	- Goal is to make a model to relate to variance, skewness, and kurtosis
		- Naturally fits into the 3 options in [[Vega (Smile) Trading]]
- Generalizing [[Bachelier Option Model]] and [[Black-Scholes]] with a quadratic term to capture fat tails
- You solve a PDE with local volatility:
$$\frac{\partial C}{\partial t} + \frac{\sigma^2(F)}{2} \frac{\partial^2 C}{\partial F^2} = 0, \quad C(F,T) = \max(0, F - K)
$$
- Uses the method of pertubation (like a taylor series applied to PDEs)
## Solution
$$C(F,t) = C_{BC}(F,t) + V_N \left( v_{QN}(K,F) + \frac{c}{6} \sigma_A^2 \tau \right)$$
- $C_{BC​}(F,t) =$ Bachelier option price
- $V_N = \sqrt{\tau} \times n \left( \frac{F - K}{\sigma_A \sqrt{\tau}} \right)$ = Normal [[Vega]] = square root of time * normal density at a certain moneyness
	- n = normal density at given moneyness
- $v_{QN}(K,F) = a + \frac{b}{2} (F+K) + \frac{c}{3} (F^2 + FK + K^2)$ - quadratic normal correction
	- **Calibration of a,b,c** -> these are changed daily depending on realized market conditions day to day
		- ATM Straddle → **Variance**
		- Costless Collar → **Skewness**
		- OTM Strangle → **Kurtosis**
- $\sigma$ = ATM bachelier normal vol