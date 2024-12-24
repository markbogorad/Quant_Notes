up:: [[Home]]
tags:: #MOC 
# Q/KdB+ MOC
- Datatypes
- 
## Q/SQL
- Retriiving tables
	- Simply call their name
- Main functions:
	- count --> counts number of rows in table
	- cols --> number of columns in table
	- meta --> returns table schema
		- t --> data structure
		- f --> foreign key (way of establishing relationships between tables)
		- a --> attributes (telling your data to improve perfomance like a sort)
- Selecting columns from a dataset
	- `select` `column_1, column_2, column_3` `from` `dataset`
- Filtering
	- Ex: date contrasint
		- `where` date = `min` date
	- Ex: greater than
		- `tip` > 20, where tip is a column capturing tip amounts for taxis
- Data partitioned kdb database (columnar based filtering)
	- ![[Pasted image 20240707223957.png]]
		- Papers are columns
		- green folders are data tables
		- orange are dates
- Commands
	- `\t` --> gives time it takes to execute, answer is in miliseconds
- Assignment operator --> `:`
	- Ex --> `total: fare + tip, fare, tip from trips where tip>0`
- Index counting operator
	- `i`
	- Ex: `select count i from trips where date = min date, passengers = 2`
		- Will give you all trips on the earliest date with 2 passengers (gets it from trips table)
- Aggregations
	- Count
	- Min
	- Max
	- avg
	- med (median)
- Grouping
	- Done with `by`
	- Ex: `select fare by vendor from jan09`
	- Result is a key table
	- Ex: getting number of records by day
		- `select count i by date from jan09`
- `fby` --> filter by
- `show` --> outputs the value of a table without re-printing it
- `~` --> equality symbol
	- 1B means equal, 0B means not equal
- deleting
	- `delete` x `from` y
- Temopral arithmetic 
- `xbar`
## Joins
- Left join
	- Merging all the contents of the table on the right into a join table with the left as the main
	- Left table can be keyed or unkeyed
		- Right must be keyed
			- A keyed table --> When a table is **keyed**, it essentially becomes a map or dictionary where the key columns serve as the unique identifier for each record. This allows for efficient searching, joining, and merging based on these key columns.
- As of join
	- join related to time
	- left once again is the base
	- having both columns keyed can improve prefomance 
## Data Structures
- List
	- Tables and their underlying columns are actually lists
- Sublist
	- a
- Sorting
	- asc (ascend keyword)
	- distinct (unique values in a list)
- Type casting
- Till
- 
## Functions

## Loading Data



[Time Series Database Lectures #4 - Fintan Quill (Kdb+) - YouTube](https://www.youtube.com/watch?v=AiGdfmxEP68)