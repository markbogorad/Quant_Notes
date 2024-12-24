up:: [[Derivatives MOC]]
tags:: #Finance 
# Gamma Scalping
- Used by [[Market Makers]] to have as little risk on as possible by [[Delta Hedging]]
	- Reduces directional risk --> goal is to have changes in the underlying do nothing to your portfolio
## How it Works
- **Essence:** make money off the [[Delta]] hedge, profit comes from buying low and selling high during hedging. Only works if price increases, then goes back down to one of the prior lower levels. If price decreases, you lose
	- Strategy will only work if you are long [[Gamma]]
- As delta accumulates towards the underlying, you make profit
- Basically, we are scalping deltas accumulated through gamma

![[Pasted image 20240629141027.png]]

- Period to period price change:
	- Move of underlying = average delta across the move
	- New price = old price + delta across the move
- Whenever price increases you add to the hedge (see dfutures increased by 6)
- End result
	- Option is worth the same
	- Made a profit on underlying while hedging
	- Often times, gamma scalping is not enough to cover the natural time decay of [[Theta]]