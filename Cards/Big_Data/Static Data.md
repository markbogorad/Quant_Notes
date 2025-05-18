up:: [[Data MOC]]
tags:: #Programming 
# Static Data
- Also referred to in the industry as “domain tables” and “list of values”, amongst other terms. 
- Static data provides a means for cross-referencing numeric and other coded values to a meaningful definition.
	- Basically, its only purpose is to make XNAS into NASDAQ, more interoperable form code to market
## Purpose
- Helps interpret compact data formats
- Avoids storing full text descriptions redundantly
- Allows consistent querying, filtering, and UI presentation

|Type|Definition|Example Use Cases|
|---|---|---|
|**Global Static Data**|Used across **many asset classes / instruments**|Market types, currency codes, country codes, rating scales|
|**Data-Type Specific Static Data**|Tied to a specific **instrument or data context**|Bond day count conventions, option exercise styles, fund classification types|

---

**Global Static Data** – "Universal Decoding". Applies everywhere in the system — regardless of asset class.

|Code|Description|Table|
|---|---|---|
|`USD`|U.S. Dollar|`CurrencyCodes`|
|`XNYS`|New York Stock Exchange|`MarketCodes`|
|`LT`|Long-Term Rating|`RatingTypes`|
|`EQU`|Equity Market|`MarketTypes`|

**Data-Type Specific Static Data** – "Specialized Decoding". Only meaningful **within a specific asset context**.

#### For Bonds:

|Code|Description|Table|
|---|---|---|
|`30/360`|Thirty/360 day count|`BondDayCountConventions`|
|`YTM`|Yield to Maturity|`YieldCalculationMethods`|

#### For Options:

|Code|Description|Table|
|---|---|---|
|`EU`|European style|`OptionExerciseStyles`|
|`AM`|American style|`OptionExerciseStyles`|

#### For Funds:

|Code|Description|Table|
|---|---|---|
|`MF`|Mutual Fund|`FundTypes`|
|`ETF`|Exchange Traded Fund|`FundTypes`|

These would **not apply** to stocks or general market data — they're **scoped** to a specific context.
