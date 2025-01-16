up:: [[SQL MOC]]
tags:: #Programming  
# Nested Queries
- Includes a query within a query
## Example:
```
SELECT name FROM users WHERE age > (SELECT AVG(age) FROM users);
```
- This query retrieves the names of users whose age is greater than the average age of all users.
- Nesting happens in ()