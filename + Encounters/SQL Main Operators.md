up:: [[SQL MOC]]
tags:: #Programming  
# Operators
Certainly! Here is the table with the operators enclosed in quotes:

| **Operator Category** | **Operator**     | **Description**                                     | **Example**                                                                                |
| --------------------- | ---------------- | --------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| Arithmetic            | `'+'`            | Addition                                            | `SELECT 10 + 5;`                                                                           |
|                       | `'-'`            | Subtraction                                         | `SELECT 10 - 5;`                                                                           |
|                       | `'*'`            | Multiplication                                      | `SELECT 10 * 5;`                                                                           |
|                       | `'/'`            | Division                                            | `SELECT 10 / 5;`                                                                           |
|                       | `'%`'            | Modulus (remainder)                                 | `SELECT 10 % 3;`                                                                           |
| Comparison            | `'='`            | Equal to                                            | `SELECT * FROM users WHERE age = 30;`                                                      |
|                       | `'<>`' or `'!='` | Not equal to                                        | `SELECT * FROM users WHERE age <> 30;`                                                     |
|                       | `'>'`            | Greater than                                        | `SELECT * FROM users WHERE age > 30;`                                                      |
|                       | `'<'`            | Less than                                           | `SELECT * FROM users WHERE age < 30;`                                                      |
|                       | `'>='`           | Greater than or equal to                            | `SELECT * FROM users WHERE age >= 30;`                                                     |
|                       | `'<='`           | Less than or equal to                               | `SELECT * FROM users WHERE age <= 30;`                                                     |
| Logical               | `'AND'`          | Logical AND                                         | `SELECT * FROM users WHERE age > 25 AND name = 'Alice';`                                   |
|                       | `'OR'`           | Logical OR                                          | `SELECT * FROM users WHERE age > 25 OR name = 'Alice';`                                    |
|                       | `'NOT'`          | Logical NOT                                         | `SELECT * FROM users WHERE NOT age = 30;`                                                  |
| Bitwise               | `'&'`            | Bitwise AND                                         | `SELECT 6 & 3;`                                                                            |
|                       | `'\|'`           | Bitwise OR                                          | `SELECT 6                                                                                  |
|                       | `'^'`            | Bitwise XOR                                         | `SELECT 6 ^ 3;`                                                                            |
|                       | `'~'`            | Bitwise NOT                                         | `SELECT ~6;`                                                                               |
|                       | `'<<'`           | Bitwise left shift                                  | `SELECT 6 << 1;`                                                                           |
|                       | `'>>'`           | Bitwise right shift                                 | `SELECT 6 >> 1;`                                                                           |
| String                | `'\|\|'`         | Concatenate (some databases use `'+'`)              | `SELECT 'Hello'                                                                            |
|                       | `'LIKE'`         | Pattern matching                                    | `SELECT * FROM users WHERE name LIKE 'A%';`                                                |
|                       | `'IN'`           | Check if value is within a set                      | `SELECT * FROM users WHERE age IN (25, 30);`                                               |
|                       | `'BETWEEN'`      | Check if value is within a range                    | `SELECT * FROM users WHERE age BETWEEN 20 AND 30;`                                         |
| Other                 | `'IS NULL'`      | Check if value is NULL                              | `SELECT * FROM users WHERE age IS NULL;`                                                   |
|                       | `'IS NOT NULL'`  | Check if value is NOT NULL                          | `SELECT * FROM users WHERE age IS NOT NULL;`                                               |
|                       | `'EXISTS'`       | Check if a subquery returns any rows                | `SELECT * FROM users WHERE EXISTS (SELECT 1 FROM orders WHERE users.id = orders.user_id);` |
|                       | `'ANY'`          | Compare a value to any value in a list or subquery  | `SELECT * FROM users WHERE age > ANY (SELECT age FROM employees);`                         |
|                       | `'ALL'`          | Compare a value to all values in a list or subquery | `SELECT * FROM users WHERE age > ALL (SELECT age FROM employees);`                         |


