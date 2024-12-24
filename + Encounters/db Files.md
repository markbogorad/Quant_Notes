up:: [[SQL MOC]]
tags:: #Programming  
# .db files
- [[Database Management Systems]] files
- Used in SQLite

## Accessing in [[Python MOC]]
```
import sqlite3

# Connect to the .db file (SQLite database)
conn = sqlite3.connect('example.db')

# Create a cursor object
cursor = conn.cursor()

# Create a table (if not exists)
cursor.execute('''
    CREATE TABLE IF NOT EXISTS users (
        id INTEGER PRIMARY KEY,
        name TEXT,
        age INTEGER
    )
''')

# Insert data into the table
cursor.execute('''
    INSERT INTO users (name, age) VALUES (?, ?)
''', ('Alice', 30))

cursor.execute('''
    INSERT INTO users (name, age) VALUES (?, ?)
''', ('Bob', 25))

# Commit the changes
conn.commit()

# Query the data
cursor.execute('SELECT * FROM users')
rows = cursor.fetchall()

# Print the data
for row in rows:
    print(row)

# Close the connection
conn.close()

```