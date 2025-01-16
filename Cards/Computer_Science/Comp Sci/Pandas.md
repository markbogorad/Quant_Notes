up:: [[Python MOC]]
tags:: #Programming 
# Pandas
- Think of this library as Pythons version of Excel
- This library is all about data handling
## Common Features
-  **Series and DataFrame:**
    - **Series:** A one-dimensional labeled array capable of holding any data type (integers, strings, floating-point numbers, etc.).
    - **DataFrame:** A two-dimensional labeled data structure with columns that can be of different types (similar to a table in a database or an Excel spreadsheet).
- **Indexing and Slicing:**
    
    - Accessing data using labels (like a dictionary) or position (like an array).
    - Supports slicing, filtering, and selecting data based on conditions.
- **Data Cleaning:**
    
    - **Handling Missing Data:** Functions like `dropna()`, `fillna()`, and `isna()` help manage missing data.
    - **Duplicated Data:** Functions like `drop_duplicates()` are used to remove duplicate entries.
- **Merging and Joining:**
    
    - **Merging DataFrames:** Similar to SQL joins, Pandas provides functions like `merge()` and `join()` to combine data from multiple DataFrames.
    - **Concatenation:** `concat()` is used to concatenate DataFrames vertically or horizontally.
- **GroupBy Operations:**
    
    - The `groupby()` function allows splitting data into groups, applying functions, and combining the results. It’s useful for aggregation, transformation, and filtering operations.
- **Data Transformation:**
    
    - Functions like `apply()`, `map()`, and `applymap()` allow applying custom functions to Series or DataFrame elements.
    - **Reshaping Data:** Pivot tables (`pivot()`, `pivot_table()`) and stack/unstack operations enable reshaping data for better analysis.
- **Date and Time Handling:**
    
    - Pandas has strong support for handling date and time data with the `datetime` module. Functions like `to_datetime()`, `date_range()`, and resampling operations simplify time series analysis.
- **Input/Output Operations:**
    
    - Pandas can read and write data from/to various formats including CSV (`read_csv()`), Excel (`read_excel()`), SQL databases (`read_sql()`), and more.
- **Descriptive Statistics:**
    
    - Pandas provides built-in functions like `describe()`, `mean()`, `std()`, `min()`, `max()`, `quantile()`, and more for summarizing and describing data.
- **Plotting:**
    
    - Basic plotting capabilities are integrated with Matplotlib, allowing you to generate plots directly from DataFrame and Series objects using the `plot()` method.