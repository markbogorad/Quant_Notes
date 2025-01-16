up:: [[Python MOC]]
tags:: #Programming 
# Concatenation
- [[Merging Datasets (Python)]] or combining them (as well as other objects like strings, lists, and more)
- Done with a + operator
- In [[Pandas]]
	- You concatenate by row or by column
	- **Axis**: You can concatenate along the rows (`axis=0`) or along the columns (`axis=1`).
		- ![[Pasted image 20240820201429.png]]
	- **Similar to Merging**: While concatenation is similar to merging, it is more about stacking DataFrames on top of each other or side by side, rather than aligning them based on keys or indices.
	- **Handling Indices**: When concatenating, you can choose to ignore the index, or you can let Pandas handle overlapping or mismatched indices in different ways.
## More Specific Concatenation -> .concat
- When you want a more unique way of merging the datasets
- Some options:
	- **`ignore_index=True`**: This argument can be used to reset the index in the resulting DataFrame after concatenation.
	- **`keys` parameter**: You can provide keys to create a hierarchical index in the resulting DataFrame.
	- **`join`**: Determines how to handle indexes and columns that do not align. Options are `outer` (default, union) and `inner` (intersection).
	
```
result_ignore_index = pd.concat([df1, df2], axis=0, ignore_index=True)
print("Concatenated with ignore_index=True:")
print(result_ignore_index)
```

