up:: [[Oil Markets MOC]]
tags:: #Finance 
# Physical Commodity Trading
- OTC transactions on any kind of commodity
	- Ex: can arrange a specific octane delivery in location X
		- In fina ical markets you need to buy RBOB and cross hedge, etc
- Trading is benchmarked to financial futures
	- Ex: buy 91 octane at RBOB + 0.05 per gallon
		- Differentials account for transportation costs, quality adjustments, and local supply/demand
- Delivery
	- **FOB (Free on Board)**: buyer picks it up
	- **CIF (Cost, Insurance, Freight)** the seller delivers
- Trading 
	- Done in massive volumes (eg 100,000+ barrels is normal)
		- AKA cargo size
### Example of a Physical Gasoline Trade
- Let's say a trader at **Vitol** wants to buy 91-octane gasoline in New York Harbor
1. **Call or message** a supplier (e.g., **Marathon Petroleum**).
2. Negotiate a deal:
    - **Buyer (Vitol):** "I'll take 50,000 barrels of 91-octane at RBOB + $0.07 per gallon, FOB NYH."
    - **Seller (Marathon):** "Agreed, delivery between March 10-15."
3. They sign a contract, and logistics (tankers, barges, storage) are arranged.

## Connection to Financial Markets
- Physical traders hedge with physical futures
	- Ex: buying RBOB if they have a physical short
	- [[Basis Risk]]

### What Do Quants Do in Physical Trading?
1. **Statistical Arbitrage in Physical Flows**
    - Identifying mispricings between **regional price differentials** (e.g., Gulf Coast vs. New York Harbor gasoline).
    - Analyzing the spread between **physical and paper markets** (e.g., RBOB futures vs. real cargo prices).
2. **Optimizing Storage & Logistics**
    - Using machine learning or optimization models to **determine the best time to buy/sell gasoline, crude, or diesel based on storage capacity and financing costs**.
    - Modeling refinery margins and crack spreads to **predict refinery behavior**.
3. **Forecasting Supply & Demand**
    - Using **satellite data, pipeline flows, and shipping reports** to predict physical shortages or surpluses.
    - Leveraging **AI/ML models** to predict when refiners will ramp up or slow production.
4. **Hedging & Derivatives Trading**
    - Designing **quant-driven hedging strategies** to minimize exposure to price swings in physical cargoes.
    - Structuring **dynamic hedging programs** for traders who manage physical barrels.
5. **Risk Management & Stress Testing**
    - Quantifying risk in **physical contracts** (e.g., counterparty default risk, logistics risk).
    - Simulating potential losses based on **disruptions in supply chains** (e.g., hurricanes, refinery outages).