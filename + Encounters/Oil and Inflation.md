up:: [[Oil Markets MOC]]
tags:: #Finance 
# Oil and Inflation
- Oil futures tend to rise with rising inflation
	- One of the only assets that does this
- This is because oil directly passes through onto CPI via gas prices
- 5y5y forward breakeven rate
	- 5 year inflation measured by 5 year forwards
		- Approximated with twice 10 year inflation minus 5 year inflation
	- This actually closely follows WTI futures, useful for forecasting
		- *Level* of commodity changes with % change in CPI
- Oil has been a superior hedge to unexpected changes in inflation when compared to gold and real estate
	- Pension funds use oil actually
	
![[Pasted image 20250113114242.png]]

## Bidirectional Causality
- Oil causes inflation by hitting CPI directly
- Inflation hit oil via forward expectations, which adjust hedging behavior now
## Oil and Inflation Quant Trading
- Trading inflation swaps
	- Opportunity exists because of the trading speed mismatch between liquid futures and OTC inflation swaps
	- Gasoline drives short term inflation, but with a lag due to OTC inflation swap nature
	- The trading strategy effectively trades the lag by creating a [[Cross-Asset Spread]]
	- I.e., when gasoline moves significantly, but inflation lags behind, you trade
		- Similar to [[Energy Statistical Arbitrage]]
		- By entering at high dislocation levels, the strategy doesn't require as high precision to win
	- **Setup:** key is to split energy vs non energy driven inflation
		- $i = \omega p \left( \frac{F(T)}{F(t_0)} - 1 \right) + (1 - \omega) i_x$
		- where: 
			- $(i)$: Total inflation rate.
			- $(R(T))$: Retail gasoline price at time 
			- $(T)$. \item $(R(t_0))$: Retail gasoline price at the base time $(t_0)$. 
			- $(\omega)$: Weight of gasoline in the CPI basket. 
			- $(i_x)$: Ex-gasoline inflation
			- The pass-through rate $(p)$ reflects how changes in RBOB futures prices $(F)$ translate into retail gasoline prices $(R)$
	- **Signal:** differential between current inflation and historical inflation crossing a certain threshold $\epsilon$
		- $\pi(S_t) = \begin{cases} -1, & \text{if } i_{x,t} - i_h > \epsilon \\ 1, & \text{if } i_{x,t} - i_h < -\epsilon \\ 0, & \text{if } |i_{x,t} - i_h| \leq \epsilon \end{cases}$
	