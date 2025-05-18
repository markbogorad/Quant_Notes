up:: [[Oil Markets MOC]]
tags:: #Finance 
# Sticky Moneyness
- Not a recommended way to do it
- Assumes that volatility shifts in parallel and retains it's entire smile (sticks to moneyness)
- Volatility will increase for every strike as futures move
	- Makes skew delta ALWAYS positive, meaning you're always going to overhedge
$$v(K,F)=v_0-\beta(K-F)$$
- Beta captures how much vol changes as moneyness changes

![[Pasted image 20250304130204.png]]

## Practical Example
- Black Scholes delta = 0.56
- Beta = 0.004
- $V_{BL}\frac{\partial v}{\partial F}$ = 20 (predictive Delta hedge adjustment)
- Net delta = $0.56 + 0.004 * 20$ = 0.64 -> buy 68 futs to hedge

## Why it's bad
- It exacerbates the asymmetry