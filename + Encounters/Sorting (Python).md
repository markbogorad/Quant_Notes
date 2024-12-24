up:: [[Python MOC]]
tags:: #Programming 
# Sorting
- Sorting in Pandas DataFrames involves arranging the rows or columns in a specific order based on the values in one or more columns or the index. 
- This operation is crucial for data analysis, as it helps in organizing and viewing data in a meaningful way.

- Pandas provides several methods to sort DataFrames, with the most commonly used being `sort_values()` and `sort_index()`.

## Sort_values
- Syntax:
	- `df.sort_values(by, axis=0, ascending=True, inplace=False, kind='quicksort', na_position='last')`
- **`by`**: Specifies the column(s) to sort by. You can pass a single column name as a string or multiple column names as a list.
- **`axis`**: Sort along the index (`axis=0`, default) or along columns (`axis=1`).
- **`ascending`**: Sort in ascending order (`True`, default) or descending order (`False`). You can pass a list of booleans if sorting by multiple columns.
- **`inplace`**: If `True`, the sorting operation will be applied directly to the DataFrame, modifying it in place. If `False`, a new sorted DataFrame is returned.
- **`kind`**: Specifies the sorting algorithm (e.g., 'quicksort', 'mergesort', 'heapsort').
- **`na_position`**: Determines the position of `NaN` values, either at the 'first' or 'last'.

- Example:
```
	# Sort by Age with NaN values at the start 
	sorted_df = df_with_nan.sort_values(by='Age', na_position='first')
	print(sorted_df)
```
## Sort_index
- Syntax:
	- `df.sort_index(axis=0, ascending=True, inplace=False, kind='quicksort', na_position='last')`
- **`axis`**: Sort by row index (`axis=0`, default) or by column labels (`axis=1`).
- **`ascending`**: Sort in ascending (`True`, default) or descending (`False`) order.
- **`inplace`**: If `True`, modifies the DataFrame in place. If `False`, returns a new sorted DataFrame.
- **`kind`**: Specifies the sorting algorithm.

- Example:
```
# Sort by column labels sorted_df = df.sort_index(axis=1) 
print(sorted_df)
```