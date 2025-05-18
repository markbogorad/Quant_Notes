sup:: [[Data MOC]], [[SQL MOC]]
tags:: #Programming 
# SQL Join
- Queries data from multiple tables - matching by a specific column 
![[Pasted image 20250506120819.png]]
```
SELECT 
    Student.[Student ID],
    Student.[Last Name],
    Student.[First Name],
    Student.Email,
    Student.[Department ID],
    Department.Department
FROM 
    Student
JOIN 
    Department
ON 
    Student.[Department ID] = Department.[Department ID];

```
## JOIN vs INSERT
- INSERT adds new data and modifies the table, JOIN is a view-only operation
```
INSERT INTO IntradayTrades (Symbol, Date, Open, Close)
VALUES ('AAPL', '2022-02-04', 137.72, 138.20);
```

## Implicit Join (Foreign Key Join)
- Foreign key join: `Stocks.MarketID = Markets.MarketID`