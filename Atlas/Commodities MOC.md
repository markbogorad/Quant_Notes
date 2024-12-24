up:: [[Home]]
tags:: #MOC 
# Commodities MOC
## Energy Markets General
- Physical vs Financial Markets
	- Physical: actual making or taking delivery of the commodity
		- Economics of physical markets (retail market (i.e. to end use customer))
			- Demand is inelastic
			- Limited storage in retail markets --> consumers cant always buy when prices are low or sell all stored products when prices are high because there is not enough storage
			- Not mane substitutes
			- Necessity factor --> consumers MUST buy at times, otherwise there will be blackouts, etc
	- Financial: no direct delivery of commodity, just an exchange of cash
- [[Physical vs Financial Energy Markets]]
- [[Retail vs Wholesale Energy Markets]]
- [[Federal Energy Regulatory Commission (FERC)]]
## Natural Gas
- [[Natural Gas]]
- [[Natural Gas Industry]]
- [[Natural Gas Storage]]
- [[Natural Gas Delivery]]
- [[Natural Gas Supply and Demand]]
## Electricity
- [[Electricity]]
- [[Electricity Storage]]
- [[Electricity Usage]]
## Crude Oil & Petroleum
- [[Crude Oil]]
- Business of producing oil is like a call option on oil
	- Either business moves ahead and profits cover costs of production and exploration or it doesn't
- Oil has no universal spot price -> a unique market in this sense
- Most effective way to move oil is via pipelines or tankers for cross continent
- Spread options -> options on the price difference between oil in 2 places
- Largest players in oil market are actually hedgers (storage trader)
	- Storage is like a real option
- Owning a refinery that processes oil is like an option on the spread between refined products and crude inputs
- Fun facts
	- World consumes 100M barrels per day
	- 2Bn barrels are traded per day across WTI and Brent
	- When adding futures, derivatives, and OTC, trading volume is 50X consumption
- Oil exchanges -> barrels released to traders in exchange for barrels later
- Government enabled arbitrage around covid time
	- Ex:
	- US govt offered oil from the SPR (strategic petroleum reserves) to traders in exchange for more oil to be traded back later
		- Strategically set an implied loan return rates via returning more barrels (9.1% more barrels), replenishing SPR
			- This only made sense (to borrow at a huge rate of 9.1%) because of the steeply backwardated curve [[Contago & Backwardation Markets]]
			- Arbitrage for trader: borrow from US govt at 9%, sell these barrels in spot market, buy 30-month futures at 20% discount and take delivery at 30 months
- Oil own rate: convenience yield
- Storage carry trade
	- Gives traders an option on time -> can carry and sell when convenient
	- Typically hedged by selling futures (so they are non directional)
	- No arbitrage condition: $F(t,T) \leq S(t) + U + R$
		- Futures price cant be higher than spot + convenience yield + cost of finanicng
- Cheapest way to store oil
	- underground in salt caverns (SPR does this)
- Higher movement fees raise the steepness of contango
- Continuous time equation for commoditiy forward pricing
	- $F(t,T = S(t)e^{(r+u-y)(T-t)}$
	- $b = y - u$
		- Own rate = benefits of consumption - cost of storing
- Refineries posses superior pil inventory knowledge
- Roll yield -> own rate of the commodity 
	- intrinsic value vs cost of storage paradigm
	- Financial traders approximating own rate
		- Buy nearest future and roll it to the next maturity = roll yield
	- Roll yield = $F(t,T)=S(t)e^{-j(T-t)}$
		- Where $j = \frac{1}{T-t} * ln(\frac{S(t)}{F(t,T)})$
	- Can be thought of as the spread between oil own rate of interest and the USD rate of interest
## Commodity Markets and Trading
- Oil firms need investment grade credit rating
	- Allows them to fund activities and infrastructure
## Market Manipulation