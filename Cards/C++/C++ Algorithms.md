up:: [[C++ MOC]]
tags:: #Programming
# Algorithms
- Set of **predefined functions** that preform **operations** on **containers**
- Part of the [[STL Implementation]]
- Algorithms are generic: work with any data type
	- Defined by [[Iterators]]
- Examples of algorithm functions
	- Sorting, searching, counting, transforming, and manipulating contents of **containers**, such as arrays, vectors, and lists
## Some common algorithms
1. ***Non-modifying* Sequence Operations:** These algorithms perform operations on sequences without modifying the elements. Examples include `std::find`, `std::count`, `std::accumulate`.
    
2. ***Modifying* Sequence Operations:** These change the elements of the sequence in place. Examples include `std::copy`, `std::remove`, `std::replace`.
    
3. **Partitioning Operations:** Used to rearrange elements based on a predicate function, such as `std::partition`.
    
4. ***Sorting* Operations:** Include algorithms for sorting and related operations, such as `std::sort`, `std::partial_sort`, `std::nth_element`.
    
5. **Binary Search Operations (on sorted ranges):** These algorithms, like `std::binary_search`, `std::lower_bound`, and `std::upper_bound`, are used to perform efficient searches on sorted sequences.
    
6. **Set Operations (on sorted ranges):** Include algorithms that treat sequences as sets and perform set operations like union, intersection, difference, and symmetric difference, such as `std::set_union`, `std::set_intersection`.
    
7. **Heap Operations:** Algorithms that manage a sequence as a heap, including `std::make_heap`, `std::push_heap`, `std::pop_heap`.
    
8. **Min/Max Operations:** Used to find minimum or maximum elements, such as `std::min`, `std::max`, `std::minmax_element`.
    
9. ***Numeric* Operations:** Perform numerical computations on sequences, including `std::iota`, `std::accumulate`, `std::inner_product`.

10. **Counting operations:** Count the number of elements smaller than a certain number `std::count_if`, program accepts a [[Functors]]

## Example:
```
#include <algorithm>
#include <vector>
#include <iostream>

int main() {
    std::vector<int> vec = {4, 1, 3, 5, 2};
    std::sort(vec.begin(), vec.end());

    for (int val : vec) {
        std::cout << val << " ";
    }
    // Output: 1 2 3 4 5
    return 0;
}
```
- Uses `std::sort`