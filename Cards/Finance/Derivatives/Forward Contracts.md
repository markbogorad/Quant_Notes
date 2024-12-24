up:: [[Derivatives MOC]]
tags:: #Finance 
# Forward Contracts
- Traded OTC
	- Tailor made for specific situation bilaterally
	- Has [[Credit Risk]]
	- Can trade out of a forward even though its highly tailored, OTC, and party-to-party:
		- Clauses for assigning the contract to a 3rd party can be made (aka assigning the contract)
		- Can do a cash settlement instead of the underlying
		- Can enter an exact offset of your forward (essentially assigning the contract with extra steps and [[Credit Risk]] from the counterparty)
- See [[Forward and Future Key Differences]]
- Move 1:1 with the underlying
- [[Futures Contracts]] are a subsection of forwards
- *Unique leverage factor*: no money exchanged until end of contract
## Long Forward
- **Payoff**
	- $St - F$
	- $\text{Market Price at Maturity} - \text{Agreed Forward Price}$
		- To succeed: $St > F$
			- This means that the market price in the future is higher than the agreed forward, so you got a better deal
## Short Forward
- **Payoff** - reverse of long
	- $F - St$
	- $\text{Agreed Forward Price} - \text{Market Price at Maturity}$
		- To succeed: $F > St$
	- Profits are fixed: your profit is the total value of underlying amount * forward price
		- Essentially you make what you get paid for on your goods, if this is above future market value you made a good trade
## Pricing F 
$$F=S(1+r_T)^T$$
- S is the spot price
- The fair price (F) is essentially the future value of the spot rate, compounded at an interest rate r for time period T
- Holds because otherwise there would be arbitrage
	- Could replicate this with bonds otherwise: [[Bond Spot Rates]]
- **Pricing with extras**
	- **With dividends**
		- $F = (S - I)(1+r_T)^T$
			- I is the PV of the dividend income stream
	- **Continuous Dividends**
		- $F = (S - I)e^{(r-q) \cdot T}$
			- where $I$ is the present value of the continuous dividend $Xe^{-rT}$ (X being underlying price)
			- $q$ is the rate of dividend payments
	- **With storage costs and convenience yield**
		- $F = (S + U - Y)(1+r_T)^T$
			- U is the PV of storage costs $= \frac{\text{Monthly Storage Cost}}{1+\text{Risk Free Asset}^\frac{\text{months elapsed}}{12}}$
			- Y is the PV of the convenience yield (premium of having asset on hand)
	- **Currency Forward** [[FX MOC]]
		- $F_T = S \frac{(1 + r_T)^T}{(1 + r_{f,T})^T}$
			- S is the current exchange rate (price of 1 unit of FX in domestic currency)
			- $r_T$ is the domestic interest rate
			- $r_{T,f}$ is the foreign interest rate