up:: [[Python MOC]]
tags:: #Programming 
# Linear Search
- See [[Linear Search]]
### How Linear Search Works
1. Start from the first element of the list.
2. Compare the target value with the current element.
3. If the current element is equal to the target value, return the index of the current element.
4. If the current element is not the target value, move to the next element.
5. Repeat steps 2-4 until the target value is found or the end of the list is reached.
6. If the end of the list is reached and the target value is not found, return -1 (or indicate that the target is not in the list).

## Implementing:
```
def linear_search(arr, target):
    """
    Perform a linear search for the target in the given array.
    
    Parameters:
    arr (list): The list to search through.
    target: The value to search for.
    
    Returns:
    int: The index of the target if found, otherwise -1.
    """
    for index, value in enumerate(arr):
        if value == target:
            return index
    return -1

# Example usage
my_list = [10, 20, 30, 40, 50]
target_value = 30

result = linear_search(my_list, target_value)

if result != -1:
    print(f"Element found at index {result}")
else:
    print("Element not found")

```