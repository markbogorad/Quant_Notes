up:: [[Oil Markets MOC]]
tags:: #Finance 
# Oil Options
- Standard oil options expire T-3 days prior to corresponding futures
- Most options are American
	- Early exercise feature can essentially be ignored because it is rarely optimal to exercise pre expiry
- Less crowded than oil futures market
- One of the largest markets
	- Ratio of option to underlying volume is one of the bigger markets (oil and LNG are largest)
- More money per trader when compared to futures
- Data infrastructure harder to build
- Dominated by producer demand for **downside price insurance** - causing negative skewness for futures returns
- Driven by need to hedge [[Real Options]]
## Parties
![[Pasted image 20250307121539.png]]
![[Pasted image 20250303131648.png]]

- Option trading is driven by hedging imbalances [[Oil Financial Hedging Equilibrium]]
- Producers (shale producers) play the biggest role in the option markets
	- Shale producers are young companies - borrow money from bank - bank requires you to hedge with [[Put Option]]s
		- Oil producers don't want to hedge from their own will - they are bullish on production
			- Bank makes them do the bare minimum hedging buy buying puts
		- Finance puts by selling calls of equivalent value **(costless collar) - main hedging instrument**
	- Hedging [[Real Options]] with financial options
	- Most producers don't hold a lot of capital - put all their money into drilling
- Consumer side (airlines are largest player)
	- Should in theory take the opposite side of the producers (buy calls and sell puts) as they are naturally short production
	- Exposure is the refined product
	- Have bad credit risk (bad for dealers) - dealers don't want to buy their put options
	- Forced to buy volatility on refined products
	- Dealer opportunity: buy cheap call from producer and sell a refined product option to the consumer
		- Collect difference in price coming from hedging desires, but exposed to [[Basis Risk]]
- Refineries/storage companies
	- Trade options on spreads (crack spreads)
	- Exposure is on spread when refining
- Investors
	- Dealer side (banks)
		- Exposes producer and consumer 
		- Buy producers call option and sell a refined product call option to the airline
			- Dealer needs to manage basis risk
	- Retail investors
		- Speculate and typically overpay for options
	- Quant funds
		- Tend to sell options

