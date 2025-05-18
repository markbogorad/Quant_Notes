up:: [[Data MOC]]
tags:: #Programming 
# SQL List
### SELECT & Filtering
- `SELECT`: `SELECT Symbol, Date FROM DailyTrades`
- `FROM`: `FROM IntradayTrades`
- `WHERE`: `WHERE Close > 100`
- `BETWEEN`: `Date BETWEEN '2025-03-24' AND '2025-03-26'`
- `AND`: `Open > 100 AND Close < 105`
- `OR`: `MarketName = 'NASDAQ' OR MarketName = 'NYSE'`
- `IN`: `MarketName IN ('NYSE', 'NASDAQ')`
- `NOT`: `WHERE NOT MarketName = 'OTC'`
- `IS NULL`: `WHERE Volume IS NULL`
- `IS NOT NULL`: `WHERE Symbol IS NOT NULL`
### Aggregations
- `MAX`: `MAX(Close)`
- `MIN`: `MIN(Open)`
- `AVG`: `AVG(Volume)`
- `SUM`: `SUM(Volume)`
- `COUNT`: `COUNT(*)`
- `ROUND`: `ROUND(MAX(Close), 2)`
- `CAST`: `CAST(AVG(Volume) AS INTEGER) AS AvgVol`
### Grouping & Sorting

- `GROUP BY`: `GROUP BY Symbol, Date`
- `ORDER BY`: `ORDER BY Date DESC`
- `HAVING`: `HAVING AVG(Volume) > 100000`
### Joins
- Join condition: `WHERE IntradayTrades.Symbol = Stocks.Symbol`
- Foreign key join: `Stocks.MarketID = Markets.MarketID`

### Math & Expressions
- Arithmetic: `(Close - Open) / Open * 100`
- Aliases: `AS`: `ROUND(MAX(...), 3) AS MaxIntrdRtn`
    
## DDL (Data Definition Language) _Defining structure_
### Create Tables
- `CREATE TABLE`:
```sql
CREATE TABLE Stocks (
  Symbol TEXT PRIMARY KEY,
  MarketID TEXT,
  ...
)
```

- `PRIMARY KEY`: `PRIMARY KEY(Symbol)`
- `FOREIGN KEY`:

```sql
FOREIGN KEY(MarketID) REFERENCES Markets(MarketID)
  ON DELETE CASCADE
  ON UPDATE CASCADE
```

- `NOT NULL`: `"Symbol" TEXT NOT NULL`
- `IF NOT EXISTS`: `CREATE TABLE IF NOT EXISTS DailyTrades (...)`

### Table Management

- `DROP TABLE`: `DROP TABLE IF EXISTS Stocks`
- `ALTER TABLE`: `ALTER TABLE Stocks ADD COLUMN Sector TEXT`
