up:: [[Derivatives MOC]]
tags:: #Finance 
# Bear and Bull Call and Put Spread Trades:
- Essence of spread trades:
	- Whenever you reach one of the bounds of your ideal range, take the opposing position with either a [[Call Option]] or a [[Put Option]] to hedge anything beyond that bound. If its 1:1 then you are immune to further movements
- Setting up
	- However you do the spread, the directions of the payoff should be counter of each other (ex: bull call spread is lower strike long and higher strike short)

## Bull Call vs Put Spread Differences

| Feature                 | Bull Call Spread                                         | Bull Put Spread                                                   | Bear Call Spread                                          | Bear Put Spread                                         |
| ----------------------- | -------------------------------------------------------- | ----------------------------------------------------------------- | --------------------------------------------------------- | ------------------------------------------------------- |
| **Option Types Used**   | Buy lower strike call, sell higher strike call           | Sell higher strike put, buy lower strike put                      | Sell lower strike call, buy higher strike call            | Buy higher strike put, sell lower strike put            |
| **Net Premium**         | Net debit (cost)                                         | Net credit (income)                                               | Net credit (income)                                       | Net debit (cost)                                        |
| **Maximum Profit**      | ***Difference between strike prices minus net premium*** | ***Net premium received***                                        | ***Net premium received***                                | ***Difference between strike prices minus net premium***|
| **Maximum Loss**        | ***Net premium paid***                                   | ***Difference between strike prices minus net premium***          | ***Difference between strike prices minus net premium***  | ***Net premium paid***                                   |
| **Profit Condition**    | Underlying asset's price at or above higher strike       | Underlying asset's price at or above higher strike                | Underlying asset's price at or below lower strike         | Underlying asset's price at or below lower strike       |
| **Loss Condition**      | Underlying asset's price at or below lower strike        | Underlying asset's price at or below lower strike                 | Underlying asset's price at or above higher strike        | Underlying asset's price at or above higher strike      |
| **Risk/Reward Profile** | Lower risk and lower reward                              | Higher risk and higher reward                                     | Higher risk and higher reward                             | Lower risk and lower reward                             |
| **Market Sentiment**    | Bullish                                                  | Bullish                                                           | Bearish                                                   | Bearish                                                 |
| **Profitability Range** | Profitable if price rises moderately                     | Profitable if price stays above higher strike or rises moderately | Profitable if price stays below lower strike or drops moderately | Profitable if price drops moderately                     |
| **Initial Cash Flow**   | Outflow (paying premium)                                 | Inflow (receiving premium)                                        | Inflow (receiving premium)                                | Outflow (paying premium)                                |