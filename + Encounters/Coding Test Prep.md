
| **Code**                                   | **Comment**                                         | **Code**                                       | **Comment**                                     |
|-------------------------------------------|----------------------------------------------------|-----------------------------------------------|------------------------------------------------|
| `nums = [1, 2, 3]`                        | `# Define a sample list`                            | `nums.index(1)`                                | `# Returns index of first occurrence of 1`      |
| `nums.append(1)`                          | `# Appends 1 to the end of the list`                | `nums.insert(0, 10)`                           | `# Inserts 10 at index 0`                       |
| `nums.remove(3)`                          | `# Removes the first occurrence of 3`               | `nums.copy()`                                  | `# Returns a shallow copy of the list`          |
| `nums.pop()`                              | `# Removes and returns last element`                | `nums.reverse()`                               | `# Reverses the list in place`                  |
| `nums.sort()`                             | `# Sorts the list in ascending order`               | `dict = {'a': 1, 'b': 2, 'c': 3}`              | `# Define a sample dictionary`                  |
| `dict.keys()`                             | `# Returns a list of dictionary keys`               | `dict.values()`                                | `# Returns a list of dictionary values`         |
| `dict.get('a')`                           | `# Returns the value for the key 'a'`               | `dict.items()`                                 | `# Returns key-value pairs as a list of tuples` |
| `dict.copy()`                             | `# Returns a copy of the dictionary`                | `dict.pop('a')`                                | `# Pops the key-value pair with key 'a'`        |
| `dict.popitem()`                          | `# Removes the most recently added pair`            | `dict.setdefault('d', 4)`                      | `# Returns value if key exists; sets to default if not` |
| `dict.update({'e': 5})`                   | `# Updates dictionary with given key-value pair`    | `set1 = {1, 2, 3}`                             | `# Define a sample set`                         |
| `set1.add(4)`                             | `# Adds item 4 to the set`                          | `set1.remove(3)`                               | `# Removes item 3 from the set`                 |
| `set1.discard(5)`                         | `# Discards item 5 (no error if not present)`       | `set1.union({4, 5})`                           | `# Returns a union of two sets`                 |
| `set1.intersection({2, 4})`               | `# Returns common elements between sets`            | `set1.difference({2, 4})`                      | `# Returns items only in first set`             |
| `set1.symmetric_difference({2, 4})`       | `# Returns all non-common elements of both sets`    | `set1.isdisjoint({5, 6})`                      | `# Checks if no common elements exist`          |
| `set1.issubset({1, 2, 3, 4})`             | `# Checks if all elements in set1 are in another set`| `set1.issuperset({2, 3})`                      | `# Checks if set1 contains all elements of another set` |
| `queue = deque(['name', 'age'])`          | `# Initialize a deque`                              | `queue.append('DOB')`                          | `# Append item from the right`                  |
| `queue.pop()`                             | `# Pop item from the right`                         | `queue.appendleft('new')`                      | `# Append item from the left`                   |
| `queue.popleft()`                         | `# Pop item from the left`                          | `queue.reverse()`                              | `# Reverse the order of deque elements`         |
| `queue.index('name')`                     | `# Returns first index of 'name'`                   | `queue.insert(1, 'inserted')`                  | `# Insert an element at index 1`                |
| `queue.count('name')`                     | `# Returns the number of occurrences of 'name'`     | `heapq.heapify(nums)`                          | `# Convert list into a heap`                    |
| `heapq.heappush(nums, 4)`                 | `# Push an element into the heap`                   | `heapq.heappop(nums)`                          | `# Pop the smallest element from the heap`      |
| `heapq.nlargest(3, nums)`                 | `# Get the 3 largest elements from the heap`        | `heapq.nsmallest(2, nums)`                     | `# Get the 2 smallest elements from the heap`   |
| `Counter(['a', 'b', 'a'])`                | `# Counts occurrences of each element`              | `collections.Counter("hello")`                 | `# Counts occurrences of characters in string`  |
| `Counter.update("abc")`                   | `# Updates the counter with new items`              | `counterObject.most_common(1)`                 | `# Returns the most common element`             |
| `text.split(' ')`                         | `# Split the string by spaces`                      | `list("abcd")`                                 | `# Convert string to list of characters`        |
| `"hello".strip()`                         | `# Removes leading and trailing spaces`             | `"HELLO".lower()`                              | `# Converts to lowercase`                       |
| `"abcd".isnumeric()`                      | `# Checks if all characters are numeric`            | `"hello".isalpha()`                            | `# Checks if all characters are alphabetic`     |
| `"Python3".isalnum()`                     | `# Checks if all characters are alphanumeric`       | `"HELLO".isupper()`                            | `# Checks if all characters are uppercase`      |
| `enumerate(['a', 'b', 'c'])`              | `# Attach index to list elements`                   | `zip([1, 2], ['a', 'b'])`                      | `# Combine elements from multiple lists`        |
| `map(str.upper, ['a', 'b'])`              | `# Apply function to each element`                  | `filter(str.isalpha, ["123", "abc"])`          | `# Filters elements that satisfy the condition` |
| `a[start:stop]`                           | `# Items from start to stop-1`                      | `a[start:]`                                    | `# Items from start to end`                     |
| `a[:stop]`                                | `# Items from beginning to stop-1`                  | `a[:]`                                         | `# A copy of the whole array`                   |
| `a[start:stop:step]`                      | `# Start through stop-1, stepping by step`          | `a[::-1]`                                      | `# All items reversed`                          |
| `df.loc[0]`                               | `# Access row with label/index 0`                   | `df.iloc[0]`                                   | `# Access row by integer location (0th row)`    |
| `df.loc[:, "column"]`                     | `# Access all rows for a specific column`           | `df.iloc[:, 0]`                                | `# Access all rows for the first column`        |
| `slice(start, stop, step)`                | `# Equivalent to a[start:stop:step]`                | `slice(None, None, -1)`                        | `# Equivalent to a[::-1], reverse slice`        |
| `any([0, 1, 0])`                          | `# Checks if any element is True`                   | `all([1, 2, 3])`                               | `# Checks if all elements are True`             |
| `dict.setdefault('key', 'value')`         | `# Get value for key; set to default if key not present` | `set1.difference_update({2, 3})`          | `# Removes common elements from set1`           |
| `set1.symmetric_difference_update({2, 4})`| `# Update set1 to contain all non-common elements`  | `set1.update({4, 5})`                          | `# Add elements from another set without duplicates` |
