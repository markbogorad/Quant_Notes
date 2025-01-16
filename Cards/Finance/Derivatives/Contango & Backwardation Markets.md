up:: [[Oil Markets MOC]],   [[Derivatives MOC]]
tags:: #Finance 

**Key Concept**:
- *The slope of the futures curve is essentially the cost of storage or [[Convenience Yield]]*
# Relationship to Time to Maturity
$$ F = S\times e^{(r+c-y)t}$$
- As a rule of thumb -> **price will always converge to current spot rate**
- It depends whether that specific market shows that it needs the asset on hand (backwardation) vs it needing to defer holding it due to storage costs (contango)
## Contango
- Futures price > current spot price
- Most commonly due to **cost of carry** associated with the underlying --> costs money to store and this needs a premium
	- For a future, this shapes out to be a premium because the counterparty pays storage costs for you
		- The closer you get to maturity, the less storage costs, the less they take of a premium
## Backwardation
- Futures price < current spot price
- Most commonly due to **convenience yield** associated with the underlying --> market wants the asset on hand now (likely due to shortages)
	- For a future, this would shape out to be a discount as you are getting deferred possession of something you want now
		- The further you get from maturity, the further you are from receiving that convenience yield --> cheaper future

## Spot Price Over Time

![[Pasted image 20240625202001.png]]

## Future Price Over Time

![[Pasted image 20240625202019.png]]
- Contago: futures price falls, spot price rises --> convergence
	- People want the underlying later
	- *Spot increase logic:* will pay more for others to store
	- *Futures decrease logic*: will pay more to get ahold of the asset later
- Backwardation: futures price rises, spot price falls --> convergence
	- People want underlying now
	- *Spot decrease logic:* will pay more for asset now, less for asset later
	- *Futures increase logic:* will pay less to get asset a longer time frame away
- Converge towards spot price over time regardless