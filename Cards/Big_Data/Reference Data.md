up:: [[Data MOC]]
tags:: #Programming 
# Reference Data
- Reference data provides static, structural descriptors — like who the entity is, what the security is, and where it trades.
	- Reference data ensures data linkage and integrity across systems.
- It is essentially the [[Primary Key]] of [[Relational Databases]]
- Think of reference data as providing the “scaffolding” for a schema:
	- **Markets** table → `MarketID` (primary key)
	- **Stocks** table → `Symbol` (primary key)
	- **Issuers** table → `IssuerID` (primary key)
- These are all reference data tables, each with their own primary keys, which are then used as foreign keys in [[Business Data]] tables like `DailyTrades` or `IntradayTrades`.
## Key Functions
- Provide unique identification (classify)
-  provide basic descriptive information that fully defines the individual data items identified by the unique identification

![[Pasted image 20250505214542.png]]

- **Primary (Backbone):** Identifiers Define a universal internal identity for an entity across systems
	- [[Primary Key]]
- **Data Source Identifiers:** Vendor- or source-specific codes that point to the same entity
	- Something that comes from an external ID like someone elses primary key for example
		- [[CUSIPS]], ISIN, DUNS, etc
```
|Field|Type|
|---|---|
|`SymbolID`|**Primary Identifier**|
|`CUSIP`|Data Source Identifier|
|`RIC`|Data Source Identifier|
|`ISIN`|Data Source Identifier|
```
