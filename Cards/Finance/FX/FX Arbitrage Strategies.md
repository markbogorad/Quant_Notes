up:: [[FX MOC]]
tags:: #Finance 
# Arbitrage Strategies
## Triangular Arbitrage
- Exploiting discrepancies in exchange rates by swapping through 3 different currencies

**Example:**
- Assume the following exchange rates:
    - EUR/USD = 1.10
    - USD/GBP = 0.75
    - EUR/GBP = 0.82
- Steps:
    1. Start with 1 million EUR.
    2. Convert EUR to USD at EUR/USD = 1.10: 1,000,000 EUR * 1.10 = 1,100,000 USD.
    3. Convert USD to GBP at USD/GBP = 0.75: 1,100,000 USD * 0.75 = 825,000 GBP.
    4. Convert GBP to EUR at EUR/GBP = 0.82: 825,000 GBP / 0.82 = 1,006,097.56 EUR.
    
    - Profit: 1,006,097.56 EUR - 1,000,000 EUR = 6,097.56 EUR.
    
## Covered Interest Rate Arbitrage
- Taking advantage of interest rate differentials between two countries ([[The Carry Trade]]), while simultaneously covering exchange rate risk with a [[Forward Contracts]]

**Example:**
- Assume:
    - Interest rate in the US (i_US) = 2%
    - Interest rate in the UK (i_UK) = 4%
    - Spot exchange rate (S) = 1.30 USD/GBP
    - Forward exchange rate (F) = 1.28 USD/GBP
- Steps:
    1. Borrow $1,000,000 in the US at 2% annual interest.
    2. Convert $1,000,000 to GBP at the spot rate of 1.30: $1,000,000 / 1.30 = 769,230.77 GBP.
    3. Invest the 769,230.77 GBP in the UK at 4% annual interest: 769,230.77 GBP * 1.04 = 800,000 GBP.
    4. Enter into a forward contract to convert the 800,000 GBP back to USD at the forward rate of 1.28: 800,000 GBP * 1.28 = $1,024,000.
    5. Repay the US loan: $1,000,000 * 1.02 = $1,020,000.
    
    - Profit: $1,024,000 - $1,020,000 = $4,000.
## Price Latency Arbitrage
- Used in high frequency trading
- Exploiting small time delays in different markets
	- Buy low and sell high across markets before price converge

**Example:**
- Assume:
    - EUR/USD is quoted as 1.10 on Exchange A.
    - EUR/USD is quoted as 1.1010 on Exchange B.
- Steps:
    1. Buy EUR/USD on Exchange A at 1.10.
    2. Simultaneously sell EUR/USD on Exchange B at 1.1010.
    
    - Profit per unit: 1.1010 - 1.10 = 0.0010 USD.
    - For a trade size of 1,000,000 EUR, the profit would be: 1,000,000 * 0.0010 = $1,000.