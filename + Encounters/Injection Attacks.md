up:: [[Computer Science MOC]]
tags:: #Programming  
# Injection Attack
- Type of security vulnerability that allows an attacker to interfere with the [[Queries]] made to a database by injecting malicious code into an input field
	- Commonly found in [[SQL MOC]]
- Common types
	- **SQL Injection**: Inserting malicious SQL queries into input fields to manipulate database operations.
	- **Command Injection**: Injecting system commands into an application to be executed on the server.
	- **Cross-Site Scripting (XSS)**: Injecting malicious scripts into web pages viewed by other users.
## Example
```
import sqlite3

def login(username, password):
    conn = sqlite3.connect('example.db')
    cursor = conn.cursor()
    query = f"SELECT * FROM users WHERE username = '{username}' AND password = '{password}'"
    cursor.execute(query)
    result = cursor.fetchone()
    if result:
        return "Login successful"
    else:
        return "Login failed"

# Example usage
username = "admin' --"
password = "any_password"
print(login(username, password))

```
#### Explanation of the Vulnerability
1. **Vulnerable Query**: The `query` string is constructed by concatenating user inputs directly into the SQL statement.
2. **Malicious Input**: An attacker can input `username = "admin' --"` which alters the SQL query to `SELECT * FROM users WHERE username = 'admin' --' AND password = 'any_password'`.
3. **Effect**: The part after `--` is treated as a comment, effectively bypassing the password check.
## To Avoid
- Use `?` placeholders instead of `{username}`