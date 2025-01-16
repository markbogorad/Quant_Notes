up:: [[Oil Markets MOC]]
tags:: #Finance
# Oil Own Rate
## Keynes and Fisher Framework
- Rate of return on lending barrels
- Derived from term structure of traded futures
	- Analogous to [[Fisher Equation (Inflation)]] and [[The Carry Trade]]
	- Here, oil own rate of interest can be derived simply as $b = \frac{B(T)-B(t)}{B(t)} \text{ OR } \frac{B(T)}{B(t)}-1$
		- $B$ is barrels at time $(t,T)$
- Including currency (USD)
$$S(t,T)=\frac{D(t,T)}{B(t,T)} \text{, then: } b = \frac{B(T)}{B(t)} - 1 = \frac{D(T)S(t)}{S(T)D(t)}-1 = \frac{S(t)}{S(T) * (1+r) - 1}$$
- D(t) = dollars at time t
- S(t) = spot oil price
- B(t) = barrels at time t (amount of them)
$$(1+r)=(1+b)\frac{S(T)}{S(t)}=(1+b)(1+i)$$
- where
	- $i = \frac{S(T)}{S(t)} - 1$
## In Practice
- Just use the forwards/futures to back out the rate
	- $b = r + \frac{1}{T-t} * ln(\frac{S(t)}{F(t,T)})$
- [[Contango & Backwardation Markets]]
	- Contango -> will give negative own rates
	- Backwardation -> will give positive rates
- Ex: spot price $S(t)$ is 60, forward price $F(t,T)$ is 70, risk free rate is 2.5% -> contango -> $\frac{60*1.025}{70} = 0.88$ , so we have an implied negative rate of 12%