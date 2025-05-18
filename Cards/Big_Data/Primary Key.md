up:: [[Data MOC]]
tags:: #Programming 
# Primary Key
- The primary key column is basically what you're declaring the index of your table to be
- For example,, the intraday trades table from Lab 1 has 3 primary keys - it filters by symbol, date, and timestamp
```
CREATE TABLE IntradayTrades (
  Symbol TEXT,
  Date TEXT,
  Timestamp TEXT,
  Open REAL,
  Close REAL,
  ...
  PRIMARY KEY (Symbol, Date, Timestamp),
  FOREIGN KEY (Symbol, Date) REFERENCES DailyTrades(Symbol, Date)
);
```
- Must be unique and not null (no duplicates or empty rows)
	- Means you'll never have 2 values at the same symbol, date, and timestamp