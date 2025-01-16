up:: [[Computer Science MOC]]
tags:: #Programming  
# Hashing
- One way [[Cryptography]]
- Used to transform a password into a fixed-size string of characters, which is typically a hash value
### Example of Password Hashing:
- **Password**: "mypassword"
- **Salt**: "randomsalt"
- **Hash Function**: bcrypt with a cost factor of 12

1. Concatenate password and salt: "mypasswordrandomsalt"
2. Apply bcrypt: `bcrypt("mypasswordrandomsalt", cost=12)`
3. Store the resulting hash and salt in the database.
4. When a user attempts to log in, the system retrieves the stored salt, hashes the entered password with the same salt and function, and compares the result to the stored hash. If computation is same then password is correct