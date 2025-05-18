up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# Technical Indicators
- Relative Strength Index (RSI)
	- a momentum oscillator used in technical analysis to measure the **speed and change of price movements**. It ranges from **0 to 100** and is commonly used to identify **overbought** or **oversold** conditions in a security.
	- $\text{RSI}= 100-\frac{100}{1+RS}$
		- $RS = \frac{\text{Average Gain}}{\text{Average Loss}}$ over 14 days
		- Overbought >70
		- Oversold <30
- Moving Average Convergence Divergence (MACD)
	- Shows the relationship between 2 moving averages
	- Ex:
		- $MACD = EMA_{12} - EMA_{26}$
	- If crosses above trend line = bullish
	- If crosses to below trend line = bearish
- Open, high, low, close, bid-ask spread, volume