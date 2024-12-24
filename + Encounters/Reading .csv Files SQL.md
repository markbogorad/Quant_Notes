up:: [[SQL MOC]]
tags:: #Programming  
# Reading CSVs
- This method is a [[Python MOC]] integration
## Example:
```
import sqlite3
import pandas as pd

# Step 1: Read the CSV file into a Pandas DataFrame
csv_file = 'your_file.csv'
df = pd.read_csv(csv_file)

# Step 2: Connect to the SQLite database (it will create the database if it doesn't exist)
conn = sqlite3.connect('your_database.db')

# Step 3: Write the DataFrame to a SQL table
df.to_sql('your_table_name', conn, if_exists='replace', index=False)

# Step 4: Query the database to make sure everything is working
query = "SELECT * FROM your_table_name"
df_from_sql = pd.read_sql_query(query, conn)

# Display the DataFrame obtained from the SQL query
print(df_from_sql)

# Step 5: Close the database connection
conn.close()

```

