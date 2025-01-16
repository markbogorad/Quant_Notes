up:: [[Python MOC]]
tags:: #Programming 
# Indices
- `[]` accessor function
	- A list, string, or [[Tuple]]
	- Allows you to access elements in a collection
- Ex:
	- `my_list = [10, 20, 30, 40]`
	- `print(my_list[0])  # Outputs: 10 
	- `print(my_list[2])  # Outputs: 30`
- Negative indexing
	- Approaching the index from end to start:
		- `my_list = [10, 20, 30, 40]`
		- `print(my_list[-1])  # Outputs: 40`
		- `print(my_list[-3])  # Outputs: 20`
- Slicing --> getting bits in the middle of the index
	- `my_list = [10, 20, 30, 40, 50]`
	- `print(my_list[1:4])  # Outputs: [20, 30, 40]`
	- `print(my_list[:3])   # Outputs: [10, 20, 30]`
	- `print(my_list[2:])   # Outputs: [30, 40, 50]`
- With strings:
	- `my_string = "Hello"`
	- `print(my_string[1])  # Outputs: 'e'`
	- `print(my_string[-1]) # Outputs: 'o'`
## Indices in Context of [[Merging Datasets (Python)]]
- Related to merging data series where 1 is market data and the other is after hours
	- Compare to [[Data Transformations (Stack, Unstack, Pivoting, Melting)]]
- **Index as a Key**: When merging datasets, the index (or indices) often acts as a key that determines how rows from one dataset align with rows from another. In stock market data, indices typically represent time stamps (e.g., date and time) or unique identifiers (e.g., stock symbols).
- **Alignment**: The merge operation aligns the datasets based on these indices, ensuring that data points from each dataset correspond correctly. For example, in stock market data, aligning trading hours with after-hours trading data requires precise time matching.