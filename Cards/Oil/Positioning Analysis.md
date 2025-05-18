up:: [[Oil Markets MOC]]
tags:: #Finance 
# Positioning Analysis
- Analyzing what other players and hedge funds are actually doing
	- Assume some parties are the smart money
- Analogy: poker
	- Any idea of your opponents cards will improve your decision making
	- Tracking order flow
	- Hard in practice: overall market picture is incomplete
- [[Oil Sentiment Analysis]]
## Setup
- A [[Flow Oil Theory (Hedging Pressure)]] approach
- Some of the hedge fund positions are known
	- Commitment of Trader Reports (COT)
	- [Commitments of Traders | CFTC](https://www.cftc.gov/MarketReports/CommitmentsofTraders/index.htm)
	- [Commitments of Traders Reports](https://www.ice.com/report/122)
	- Publish positions by 4 categories
		- Hedge funds (money managers MM) - [[Risk Parity (All Weather)]]
		- Producers - storage hedgers
		- Banks (swap dealers)
		- Other reportables
## Strategy Ideas
- **Follow the flow strategy**
	- Following hedge funds simply
	- Time lag is an issue - report released Friday and they report positions Tuesday (3 day lag) and you can only bet on Monday (week lag)
	- [[Oil Momentum Risk Premia]] MA signal applied on a hedge funds position
		- Strategy is sign of momentum on their position
			- If their position today is larger than their position over last N days, we go long
			- If they buy, we buy, relative to some kind of MA
		- Short term N 2-3 weeks, long term N 8-12 weeks
	- Deeper layer: make a function that derives the actual position they have been taking (like momentum, carry, value, etc)
		- Set up their position from the COT report as a function of momentum and carry
			- Fit the approximation function to the actual position - will essentially map what hedge funds do every day
			- Mixing:
				- COT reports, 
				- a time series of historical [[Oil Momentum Risk Premia]] and [[Oil Carry Risk Premia]] signals
				- a [[Neural Network]] based extrapolation of the [[Reaction Function]]
- **Fading the crowded trade**
	- If hedge fund position is a certain large percentile larger than their historical position - you take opposite side
		- Traded is crowded
- **Shorting other reportables group**
	- They're considered to be dumb money