up:: [[Derivatives MOC]]
tags:: #Finance 
# Lattice Methods:
For computational finance: [[Lattice Methods C++]]

- The construction of a grid (lattice) to model the paths that the option price could take until expiry
- Particularly useful for American options
	- Variant in time where you can exercise early
- Applicable when [[Black-Scholes]] assumptions don't hold
	- For options with dividends and options exercised early
![[cq5dam.web.1280.1280.png]]
## Binomial Models
- The simplest lattice method (2 states)
- For each interval, the price of the underlying asset is assumed to either increase by an up factor (u) or decrease by a down factor (d).
- Assumes risk neutrality
- Recursive calculation
	- Starting at the expiration date, the model calculates the option's value at each preceding interval by considering the value in the two possible subsequent intervals (up and down).
### Formula:
![[Pasted image 20240327150006.png]]
#### Binomial for Calls
- uS: Option value in the up state (current price * move factor "u")
	- u = up move factor
	- S = underlying asset
- dS: Option value in the down state
	- d = down move factor
- X: exercise price
- Cu: payoff in the upstate 
	- Max [Price at maturity (S) - strike price (K), 0]
- Cd: payoff in the down state
	- Max [Price at maturity (S) - strike price (K), 0]
- Dcu: Down state * payoff in up state
- Ucd: Up state * payoff in the down state
#### Binomial for Puts
###### The exact reverse of the call situation:
- uS: Up state here is technically a decline in the underlying price
- dS: Down state is an increase in underlying price
- X: same exercise price
- Cu: put payoff in up state 
	- K (strike price) - S (price at maturity)
- Cd: put payoff in down state
- Dcu: Down state * payoff in up state
- Ucd: Up state * payoff in the down state

### Pricing at a Given Point in the Lattice Grid:
#### Pricing by Replication
- Essentially pricing an option by tangentially pricing all the components of a theoretical **replicating portfolio** that would have the same payoff as the call
- This approach assumes:
	1) no arbitrage between the call and replicating portfolio
	2) a perfect replicating portfolio can be created, using the underlying and risk free bonds to match the call
##### Formula: 
$$
C = \Delta S - \frac{N}{1+r}
$$
where:
C = call price (option premium)
S = current price (multiply this by delta)
Delta = captures the price movement in the underlying
$$
\Delta = \frac {c_u-c_d} {(u-d)S} 
$$
		where:
			Payoff in up state - payoff in down state) / (up state factor - down state factor) * the current price
			Cu (re-organization of formula)= 
$$
			c_u = \Delta uS - N
$$
			Cd =
$$
			c_d = \Delta dS - N
$$

N = the bonds we should short in the replicating portfolio (number of time steps)
$$
N = \frac {dc_u - uc_d} {u - d}
$$
		where:
			(Down state * payoff in up state) - (up state * payoff in down state) / up state factor - down state factor
##### Example:
![[Screenshot 2024-03-27 at 4.10.24 PM.png]]

![[Screenshot 2024-03-27 at 4.10.34 PM.png]]

#### Risk Neutral Pricing
- Assumes investors are not compensated for risk and are indifferent
- The expected future prices in the binomial tree are calculated assuming that the probability of the price moving up or down is such that the **expected return of the underlying asset is the risk-free rate**, aka "risk-neutral probability."
##### Formula:
$$
C = \frac {1}{1+r}[qc_u+(1-q)c_d]
$$
where:
	Cu and Cd: payoffs in upstate and downstate as before
	q = **risk neutral probability**
$$
	q = \frac {(1+r)-d}{u-d}
$$
			u/d: probabilities of up/down moves
##### Neutral Continuous Pricing
###### Formula:
$$
C = e^{r \Delta t}[qc_u+(1-q)c_d]
$$

**Risk neutral probability**
$$
	q = \frac {e^{r\Delta t}-d}{u-d}
$$
- e^rΔt 
	- The factor by which the risk-free asset grows in one time step
##### Example (same as replication):
![[Screenshot 2024-03-28 at 5.36.39 AM.png]]
![[Screenshot 2024-03-27 at 4.09.45 PM.png]]
