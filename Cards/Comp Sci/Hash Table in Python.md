up:: [[Python MOC]]
tags:: #Programming 
# Hash Tables in Python 
- See [[Hash Tables]]
- Uses a [[Dictionaries in Python]]
- **Initialization**: The [[__init__]] method initializes the hash table with a specified size and creates empty lists for each slot.
- **Hash Function**: The `hash_function` method computes an index based on the key.
- **Insert**: The `insert` method adds key-value pairs, handling collisions by appending to a list.
- **Get**: The `get` method retrieves the value associated with a key.
- **Delete**: The `delete` method removes a key-value pair if it exists.

## Example: 
```
# Step 1: Initialize an empty hash table (dictionary)
hash_table = {}

# Step 2: Add items to the hash table
hash_table["apple"] = 1
hash_table["banana"] = 2
hash_table["cherry"] = 3

# Step 3: Access items in the hash table
print("Value for 'apple':", hash_table["apple"])  # Output: 1

# Step 4: Remove an item from the hash table
del hash_table["banana"]

# Trying to access the deleted item will result in a KeyError
try:
    print("Value for 'banana':", hash_table["banana"])
except KeyError:
    print("'banana' not found in hash table")

```