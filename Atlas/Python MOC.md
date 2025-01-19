up:: [[Home]]
tags:: #MOC 
# Python MOC
## Snow Notes
- Python version
	- `pd.__version__`
- Dataframe = panel data
	- Dataframe to numpy array
		- `.values` function, ex: `s_pa.values`
	- Creating a dataframe
		- `df_pa=pd.DataFrame(np.array([[10, 11], [20, 21]]), columns=['A', 'B'])`
	- Accessing column by name
		- result is a Series
		- `sp500['Price'].head()`
	- Filtering a dataframe
		- `sp500_pl.filter(pl.col('Price') < 100)`
- Series = single time series
	- Slicing a series: taking a specific excerpt out
		- Ex: `s_pa[3:8]` will output column elements from 3 to 8
	- `len()`
		- Length of a series
	- `.shape`
		- Shape of the series -> a tuple that shows it's dimensions
- Indices
	- Specifying an index
		- `s2_pa = pd.Series([1, 2, 3, 4], index=['a', 'b', 'c', 'd'])`
	- Indices are typically the date
	- Examining the index
		- `.index`
	- Selecting rows by index
		- `.loc` and `.iloc`
			- loc for text, iloc for integer
			- Think of this as command + f
		- Ex: `sp500.loc[['MMM', 'MSFT']]`
			- Result is a dataframe with labels MMM and MSFT
		- Ex: time
			- `# Select dates between 2016 and 2020`
			- `msft = msft.loc['2016-01-01':'2020-12-31']`
	- Single cell lookup
		- `.at[]` and `.iat[]`
	- re-indexing
		- `s2 = s.reindex(['a', 'c', 'e', 'g'])`
	- Multiple indices (for panel)
		- `mi = s4g.set_index(['Symbol', 'Year', 'Month'])`
- Reading csv
	- `msft = pd.read_csv("https://storage.googleapis.com/public-quant/random/MSFT.csv", index_col=0, parse_dates=True)`
- Re-shaping, Re-Organizing, Aggregation
	- Concatenation (`.concat`)
		- Combining multiple series under the same dataframe
		- `pd.concat([msftA01.head(3), msftA02.head(3)])`
		- Inner join
			- `pd.concat([msftAV, aaplA], join='inner')`
	- Merging
		- Combines different dataframes under 1 super dataframe
		- `msftCVR = pd.merge(msftAR, msftVR)`
	- Pivoting
		- A macro resahping, can work as a filtering mechanism
			- Like a pivot table
		- `closes = s4p.pivot(index='Date', columns='Symbol', values='Adj Close')`
	- Stack/Unstack
		- `pd.stack`
		- `pd.unstack`
	- Melting
		- `pd.melt`
	- Grouping
		- `grouped=pd.groupby('Symbol')`
		- Can do multiple groups
			- `mcg = s4g.groupby(['Symbol', 'Year', 'Month'])`
	- Aggregation
		- `.agg()`
		- Applies a specific function (like mean) to a dataframe
		- `mig_l12.agg(np.mean)`
- Time Series
	- datetime library `import datetime`
	- Making datetime objects `dates = [datetime(2018, 8, 1), datetime(2018, 8, 2)]`
	- Converting list to datetime
		- `dti = pd.to_datetime(['Aug 1, 2018', '2018-08-02','2014.8.3', None],format='mixed')`
## Libraries
- [[sys]]
- [[Numpy]]
- [[Pandas]]
- [[Matplotlib, Seaborn, Plotly]]
	- klib, detail
	- pygwalker --> like tableau
- [[Qpython]]
- [[Streamlit]] 
- Nixtla --> time series python package
- Darts --> also time series
- sklearn
- Polars --> pandas but it has no index
## Basics
- [[Operators in Python]]
	- [[{} in Python]] -
- [[Data Types in Python]]
- [[Python General Built in Functionalities List]]
## Data Operations (Pandas Main Features)
- [[Indices (Python)]]
- [[Data Transformations (Stack, Unstack, Pivoting, Melting)]]
- [[Concatenation in Python]]
- [[Merging Datasets (Python)]]
- [[Vectorization (Python)]]
- [[Groupby (Python)]]
- [[Sorting (Python)]]
- [[Query (Python)]]
- Data Resampling --> taking data from higher to lower frequency
	- Can be done on a declared basis (the average, or the last price, etc)
## Unique Features
- [[Calling "Self" in Python]]
- [[__init__]]
- [[Classes in Python]]
- [[Computational Functions]]
- [[Docstring]]
- [[Hash Table in Python]]
- [[Linear Search in Python]] 
- [[Dictionaries in Python]]
- [[Python Loops]] 
- [[Try Statement]] 
## Data Structures
- [[Arrays DSA]]
- [[Matrices DSA]]
- Hash Maps DSA
## Algorithms
- Recursion
- 2 Pointer
- Dynamic Programming
- Breadth First Search
- Depth First Search
## Advanced Features
- [[Multithreading in Python]]



Delimiter; --> csv files
drop na vals
merge date and time


[[Coding Test Prep]]