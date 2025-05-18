up:: [[Oil Markets MOC]]
tags:: #Finance
# Oil Own Rate
- Oil own rate essentially captures the value of oil today relative to it's futures
- The derivation is the same as the concept of the [[Fisher Equation (Inflation)]]
	- Interest rate = real yield + inflation
$$\frac{B(T)}{B(t)}-1=\frac{S(t)}{S(T)}(1+r)-1$$
- Barrel at expiry / barrel today - 1
- OR
- Spot today / future at expiry (will be future spot is the assumption) * interest - 1
	- Change in futures proxies inflation
	- Interest is real yield 
## Extrapolating from Futures (Continuous Own Rate)
- In practice, you can take out the actual own rate at any given time interval (t,T) with:
$$b = r + \frac{1}{T-t} * ln(\frac{S(t)}{F(t,T)})$$
- Own rates are extremely volatile in practice (-120% to + 40%)
## Own Rate - Contango/Backwardation
- [[Contango & Backwardation Markets]]
- Backwardation -> will give positive rates (own rate exceeds risk free rate)
	- **Example:** 
		- spot price $S(t)$ is 60, 
		- forward price $F(t,T)$ is 50, 
		- risk free rate is 2.5% -> 
		- Own rate = $\frac{S(t)}{S(T)}(1+r)=\frac{60*1.025}{50} = 1.23$ , so we have an implied positive rate of 23%
- Contango -> will give negative own rates (own rate is less than risk free rate)
	- Logic: the value of your barrel is increasing in price relative to futures (expecting inflation), therefore value of a barrel today is LESS than it will be in the future, i.e. owning it is a negative interest
	- **Example:** 
		- spot price $S(t)$ is 60, 
		- forward price $F(t,T)$ is 70, 
		- risk free rate is 2.5% 
		- Own rate = $\frac{S(t)}{S(T)}(1+r)=\frac{60*1.025}{70} = 0.88$ , so we have an implied negative rate of 12%

