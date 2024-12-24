up:: [[Derivatives MOC]]
tags:: #Finance 
# Put-Call Parity
- The premia on puts and calls (on the same underlying and with he same strike price and maturity) are linked together (the same) by the concept of no arbitrage
- Holding a **long call** option and **shorting the asset** should provide the *same payoff* as holding a **put option** and holding **cash equal to the present value of the strike price.**
	- **Alternatively**, a long [[Call Option]] and a short [[Put Option]] should perfectly reconstruct the payoff of a [[Futures Contracts]], which is equal to $\frac{k}{(1+r)^t}$, see [[Relationship Between Calls, Puts, and Futures (No Arbitrage)]]
- Applies specifically to European options
$$
S + P = C + \frac{k}{(1+r)^t} \hspace{1cm} OR \hspace{1cm} C - P = S - \frac{k}{(1+r)^t} \hspace{1cm} OR \hspace{1cm} S + P = Xe^{-rT} + C
$$
where:
	$S$: Current price of underlying
	$P$: Put option premium
	$C$: Call option premium
	$k$: Strike Price
	$r$: Risk free rate of return
	$t$: Time to maturity
	$\frac{k}{(1+r)^t}$: PV of strike price, also the PV of a [[Futures Contracts]]

- Last formula is in continuous time


