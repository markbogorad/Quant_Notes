up:: [[Data MOC]]
tags:: #Programming 
# Foreign Key
- A [[Pointers]] that refers back to the [[Primary Key]]
	- A foreign key **must** reference a primary key
- Needed for the JOIN operation in [[SQL]]
- Ex: a doctors recording referencing your SSN (primary key)
```
SELECT *
FROM Stocks
JOIN Markets ON Stocks.MarketID = Markets.MarketID;
```
- Using a foreign key in `Stocks` to match the PK in `Markets`
## Defining a FK
```
CREATE TABLE Stocks (
  Symbol TEXT PRIMARY KEY,
  MarketID TEXT,
  FOREIGN KEY (MarketID) REFERENCES Markets(MarketID)
);
```
- “Hey, `Stocks.MarketID` must always match something in `Markets.MarketID`.”
- You establish a table’s ability to be **"looked up on"** by giving it a **primary key**.  Then, other tables can **“look up to it”** using **foreign keys** that reference that primary key.