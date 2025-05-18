up:: [[Data MOC]]
tags:: #Programming 
# Relational DB Goals

|**Concept**|**Definition**|**Purpose**|**Example**|**Key Tools/Techniques**|
|---|---|---|---|---|
|**Data Persistency**|Ensures that data remains stored and available **after the program ends** or a crash.|To **retain data over time**, across sessions or power loss.|Storing a trade in a `Trades` table so it's available after the app closes.|Database files (e.g., `.db`), transactions|
|**Data Normalization**|Organizing data into tables to **reduce redundancy**and improve integrity.|To save space, avoid duplication, and make updates **faster and safer**.|Separating `Customer` and `Order`tables to avoid repeating customer info in every order row.|1NF, 2NF, 3NF; Foreign Keys; E-R modeling|
|**Procedural vs. Non-Procedural Changes**|Procedural: **how** to perform a task; Non-procedural: **what** data is needed.|DBMS prefers non-procedural queries (like SQL) for flexibility and simplicity.|Procedural: `for each record, check condition`; Non-procedural: `SELECT * WHERE condition`.|SQL is **non-procedural**|
|**Data Integrity**|Ensures data is **accurate, consistent, and valid**throughout its lifecycle.|To prevent errors, maintain trust, and enforce business rules.|A `Price` field can't be negative; a `TradeDate` must exist in the calendar.|Constraints (PK, FK, CHECK), Triggers|

- **Persistency**: Keeps data safe.
- **Normalization**: Makes storage efficient and logic clean.
- **Procedural vs Non-Procedural**: Focus on _what_, not _how_.
- **Integrity**: Ensures correctness and reliability of the data.
- **Data Independency**: internal schema changes (modifying physical storage) shouldn't affect logic schema
- [[Allowing for Concurrency]]
	- Multiple read/write at the same time