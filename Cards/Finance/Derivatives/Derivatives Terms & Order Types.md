up:: [[Derivatives MOC]]
tags:: #Finance 
## Terms
- **Strike**: price at which the option can be bought or sold for 
- **Last**: this is the last traded strike price of the option (call option with 300$ strike was 50.60$)
- **Chg**: change in strike price from the previous trading session (call option with 300$ strike increased by 1.55$)
- **Bid:** The highest price a buyer is willing to pay for the option.
- **Ask (Offer):** The lowest price a seller is willing to accept for the option.
- **Liquidity** is measured by the *tightness of the bid/ask spread and the size*
- **Volume:** The number of contracts traded during the current session.
- **Open Interest (Open Int.):** The total number of outstanding contracts that are held by market participants at the end of the day.
	- A marker of option [[Liquidity]]
	- Can show trends, reversals, resistance, and support>)
- **Size:** the amount of contacts one is willing to trade at a given price (price value not included)
- **Market making:** providing a bid and ask price and size
- **Spread:** bid - ask (offer).  Described as "spread for this market is x degrees wide"
- **Paper:** parties trading against you
- **Broker:** an intermediary that takes orders from one party and finds another party
- **Tick Size:** smallest increment between 1 price and the next highest/lowest price (ex: stock price 100 and next price is 100.01, tick size is 0.01). Different products haver different tick sizes
- **Queue Priority:** determines who is first in line for a trade
	- Most common: **price time priority method**
		- Ordered by lowest bid, then by whoever put order in first


## Option order Types
- **Immediate or Cancel Order (IOC)** or **Fill and Kill (FAK)**
	- Requires all or part of the order to be executed immediately, all remaining parts are canceled
		- Buy all available size on a given price, if not enough size order is cancelled
- **Good for Day (GFD)**
	- Remains active until end of trading day or until partially or fully executed before that time
- **Good Till Cancelled (GTC)**
	- Remains active until completed or cancelled
- **All or None (AON)**
	- Order must be executed in it's entirety or not at all --> stays on book until executed
	- Not as popular of an order type
	- Used for very specific strategies and sizes -> accounting can be more trouble than it's worth for small orders 
- **Fill or Kill (FOK)**
	-  Order must be executed in it's entirety or not at all --> does not stay on book if not executed
- **One Cancels the Other (OCO)**
	- If one specifies his markets are OCO --> one of this persons orders gets executed and the other is canceled
		- Either one or the other -> used to protect from too much exposure from one direction