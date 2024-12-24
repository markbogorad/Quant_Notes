up:: [[Python MOC]]
tags:: #Programming 
# Merging Datasets
- Done based off [[Indices (Python)]]
## Types of Merge Operations
- **Inner Join**: Merges only the rows that have matching indices in both datasets.
- **Left Join**: Merges all rows from the left dataset with matching rows from the right dataset. Unmatched rows from the left dataset will have `NaN` values for columns from the right dataset.
- **Right Join**: Similar to a left join, but includes all rows from the right dataset.
- **Outer Join**: Merges all rows from both datasets, with `NaN` for any unmatched rows.
## Example: 
```
import pandas as pd

# Example Trading Hour Data
trading_data = pd.DataFrame({
    'Timestamp': ['2024-08-20 09:30', '2024-08-20 10:00', '2024-08-20 10:30'],
    'Price': [150, 152, 153]
})
trading_data['Timestamp'] = pd.to_datetime(trading_data['Timestamp'])
trading_data.set_index('Timestamp', inplace=True)

# Example After-Hours Data
after_hours_data = pd.DataFrame({
    'Timestamp': ['2024-08-20 16:30', '2024-08-20 17:00', '2024-08-20 18:00'],
    'Price': [154, 155, 156]
})
after_hours_data['Timestamp'] = pd.to_datetime(after_hours_data['Timestamp'])
after_hours_data.set_index('Timestamp', inplace=True)



# Merge the datasets
merged_data = pd.merge(trading_data, after_hours_data, how='outer', left_index=True, right_index=True, suffixes=('_trading', '_after_hours'))
print(merged_data)

```

## If Merging Different Frequencies
- Left: higher frequency
- right: lower frequency
## Merge as of
- Approximate match merging --> allows you to ignore weekends
- Similar to [[SQL]] joins
- **Purpose**: `merge_asof` is used to merge two DataFrames based on a key column, usually a datetime or a similar ordered variable, where the merge is performed "as of" a certain point, meaning it will match the nearest key that is less than of equal to the key in the other DataFrame.
- **Typical Use Case**: It is often used in financial data analysis, such as merging trading data with event data, or aligning time series that don’t have exactly matching timestamps but are close in time.
- How it works:
	- Uses .merge
	- Key parameters:
	- **`how`**: The type of merge to perform (`'inner'`, `'outer'`, `'left'`, `'right'`).
    - `'inner'`: Only include rows with matching keys in both DataFrames.
    - `'outer'`: Include all rows from both DataFrames; fill in missing values with `NaN`.
    - `'left'`: Include all rows from the left DataFrame and only matching rows from the right DataFrame.
    - `'right'`: Include all rows from the right DataFrame and only matching rows from the left DataFrame.
	- **`on`**: Column or index level names to join on. If not specified and `left_on` and `right_on` are also not specified, the merge will attempt to join on columns with the same names.
	- **`left_on` / `right_on`**: Column names in the left/right DataFrame to join on.
	- **`left_index` / `right_index`**: Use the index from the left/right DataFrame as the key for the merge.
	- **`suffixes`**: Suffixes to apply to overlapping column names in the left and right DataFrames.
- Example:
	- `pd.merge(left, right, how='inner', on=None, left_on=None, right_on=None, left_index=False, right_index=False, suffixes=('_x', '_y'))`
	