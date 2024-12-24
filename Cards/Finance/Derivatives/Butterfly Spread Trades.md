up:: [[Derivatives MOC]]
tags:: #Finance 
# Butterfly Spread Trades
- All are bets on low volatility, some more bearish some more bullish
- [[Long Butterfly Spread Trades]]
- [[Short Butterfly Spread Trades]]
- Shortcut to seeing max loss and gain for longs (Akuna Options 101)
	- Max gain = $K_2 - K_1$ - Butterfly Premium
	- Max loss = Butterfly Premium
	- Breakeven = $K_1$ + butterfly premium    and    butterfly premium - $K_3$
## Overview:

| Feature                  | Long Butterfly with Calls                                       | Long Butterfly with Puts                                     | Short Butterfly with Calls                                       | Short Butterfly with Puts                                     |
| ------------------------ | --------------------------------------------------------------- | ------------------------------------------------------------ | ---------------------------------------------------------------- | ------------------------------------------------------------- |
| **Option Types Used**    | Call Options                                                    | Put Options                                                  | Call Options                                                     | Put Options                                                   |
| **Structure**            | Buy 1 call @ $(K1)$, sell 2 calls @ $(K2)$, buy 1 call @ $(K3)$ | Buy 1 put @ $(K1)$, sell 2 puts @ $(K2)$, buy 1 put @ $(K3)$ | Sell 1 call @ $(K1)$, buy 2 calls @ $(K2)$, sell 1 call @ $(K3)$ | Sell 1 put @ \(K1\), buy 2 puts @ \(K2\), sell 1 put @ \(K3\) |
| **Strike Prices**        | $(K1 < K2 < K3)$                                                | $(K1 < K2 < K3)$                                             | $(K1 < K2 < K3)$                                                 | $(K1 < K2 < K3)$                                              |
| **Market Sentiment**     | Neutral to **slightly bullish**                                 | Neutral to **slightly bearish**                              | Neutral to **slightly bearish**                                  | Neutral to **slightly bullish**                               |
| **Profitability Range**  | *Profitable if the price stays near \(K2\)*                     | *Profitable if the price stays near \(K2\)*                  | *Profitable if the price moves away from \(K2\)*                 | *Profitable if the price moves away from \(K2\)*              |
| **Net Premium**          | Typically a net debit (cost)                                    | Typically a net debit (cost)                                 | Typically a net credit (income)                                  | Typically a net credit (income)                               |
| **Maximum Profit**       | $((K2 - K1) - \text{Net Premium Paid})$                         | $((K2 - K1) - \text{Net Premium Paid})$                      | Net premium received                                             | Net premium received                                          |
| **Maximum Loss**         | Net premium paid                                                | Net premium paid                                             | $((K2 - K1) - \text{Net Premium Received})$                      | $((K2 - K1) - \text{Net Premium Received})$                   |
| **Ideal Price Movement** | Low volatility, price near the middle strike \(K2\)             | Low volatility, price near the middle strike \(K2\)          | High volatility, price moves away from \(K2\)                    | High volatility, price moves away from \(K2\)                 |
| **Initial Cash Flow**    | Typically an outflow (paying premium)                           | Typically an outflow (paying premium)                        | Typically an inflow (receiving premium)                          | Typically an inflow (receiving premium)                       |
| **Example**              | Buy 1 call @ $50, sell 2 calls @ $60, buy 1 call @ $70          | Buy 1 put @ $50, sell 2 puts @ $60, buy 1 put @ $70          | Sell 1 call @ $50, buy 2 calls @ $60, sell 1 call @ $70          | Sell 1 put @ $50, buy 2 puts @ $60, sell 1 put @ $70          |
