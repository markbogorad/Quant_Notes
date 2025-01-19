up:: [[Oil Markets MOC]]
tags:: #Finance 
# Macro Fair Value Model
- Essentially a [[Multiple Linear Regression]] model that uses [[Cross-Asset Spread]] trading strategies as regressiors
	- Things like CAD/USD, CPI, and [[XOP]] can be a 3-factor macro model
- **Strategy:** if deviation is too far from model, you can trade off that
- Were are applying regression analysis to non stationary variables, but this is allowed because they are [[Cointegration]]-ed, similar to [[ARDL]] model with CBRE
## Additional factors list

| **Macro Tradable**         | **Macro Fundamental**       | **Oil Specific**          |
|-----------------------------|-----------------------------|---------------------------|
| Broad USD Index            | Global PMI                 | Inventory                 |
| Commodity FX Basket        | GDP Nowcast                | Carry                     |
| 5y5y Breakeven             | Economic Surprise Index    | Hedge Fund Positioning    |
| 2y-10y Interest Rate Spread| Financial Conditions Index | Refinery Margins          |
| VIX                        | Chinese Demand Index        | Option Skews              |
| Emerging Market Equity Index|                             |                           |
| Credit Spreads             |                             |                           |

