up::  [[Oil Markets MOC]], [[Quantitative Valuation MOC]]
tags:: #Finance  
# Cash and Carry Arbitrage
- No arbitrage futures condition - futures can't dislocate from spot by more than storage cost, otherwise [[Commodity Carry Trade]] would be risk free profit
$$F(T,t) \leq S(t) + U + R$$
- Inequality because of the +- infinity bounds on [[Inventories]]
- Turned into an equality when including [[Convenience Yield]]
$$F(T,t)=S_0 e ^{(r+u-y)(T-t)} OR F(T,t)=S_0 e ^{(r-b)(T-t)}$$
- If $F(T,t) > S(t) + U + R$
- **Step 1**: Buy the underlying asset in the spot market.
- **Step 2**: Simultaneously sell (short) a futures contract on the asset.
- **Step 3**: Hold the asset until the futures contract expires. 
- **Step 4**: Deliver the asset at the futures contract’s higher price to fulfill the short futures position.

The profit is made from the difference between the higher futures price and the lower spot price, after accounting for any holding (carry) costs, such as storage and financing.

## Reverse Cash-and-Carry Arbitrage
- **NEED INVENTORY TO SHORT THIS** [[Stylized Model of the Squeeze]]
- If $F(T,t) < S(t) + U + R$
- **Step 1**: Short-sell the underlying asset in the spot market.
- **Step 2**: Simultaneously buy a futures contract on the asset.
- **Step 3**: When the contract expires, take delivery via the futures contract at the lower futures price.
- **Step 4**: Use the asset from the futures contract to close out the spot market short position.

The profit here is the difference between the higher spot price and the lower futures price, adjusted for carry costs.

Will not work if supply runs out! - [[Negative Oil Prices]]