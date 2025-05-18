up:: [[Data MOC]]
tags:: #Programming 
# Metadata
- Data about data

| Data                    | Metadata                                                           |
| ----------------------- | ------------------------------------------------------------------ |
| A stock price: `173.54` | Ticker = `AAPL`, Currency = `USD`, Timestamp = `2022-02-04 09:30`  |
| A column named `Close`  | Data type = `FLOAT`, Units = `USD`, Source = `Yahoo API`           |
| A table called `Stocks` | Created = `2025-03-01`, Primary Key = `Symbol`, Row count = `5000` |
| A CSV file              | Delimiter = `,`, Encoding = `UTF-8`, Header row = Yes              |

```sql
PRAGMA table_info(Stocks); -- SQLite command to get column metadata
```
- PRAGMA modifies matedata in [[SQL MOC]]


|Command|Description|
|---|---|
|`PRAGMA table_list;`|Lists all tables|
|`PRAGMA foreign_key_list(Stocks);`|Shows foreign key relationships|
|`PRAGMA index_list(Stocks);`|Lists indexes on the table|
|`PRAGMA schema_version;`|Version info for schema|
|`PRAGMA user_version;`|User-defined DB versioning (custom control)|
