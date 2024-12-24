up:: [[C++ MOC]]
tags:: #Programming
# Containers
- Objects that **store data in memory**
- Part of the STL [[STL Implementation]]
- Pros of containers
	- Generic (can store any elements)
	- Dynamic size (automatically resize themselves)
	- Type safe
	- Efficient memory management
	- Easy insertion/deletion
	- Easy iteration [[Iterators]]
	- Has exception safety
## Main Types of Containers
#### 1. Sequence Containers
These containers maintain the order of insertion of the elements.

- **`std::vector`**: Represents a *dynamic array* that can grow or shrink in size. Offers fast random access to elements, efficient when adding or removing elements at the end. [[C++ Vectors]]
    
- **`std::deque`**: Similar to `vector`, but *designed for efficient insertion and removal of elements* at both the beginning and the end.
    
- **`std::list`**: Implements a doubly linked list. Supports efficient insertion and removal of elements from anywhere in the container.
    
- **`std::forward_list`** (since C++11): Implements a singly linked list, optimized for efficient insertion and removal of elements.
    
- **`std::array`** (since C++11): Represents a fixed-size [[Arrays]]. Offers fast random access like a *plain array, but with the benefits of container semantics. (benefits of being an STL container)*
    
#### 2. Associative Containers
These containers automatically sort their elements, typically using comparison operators or a specified comparison function.

- **`std::set`**: Stores unique elements following a specific order.
    
- **`std::multiset`**: Like `set`, but allows duplicate elements.
    
- **`std::map`**: Stores key-value pairs, with unique keys sorted by their values.
    
- **`std::multimap`**: Like `map`, but allows keys to have multiple values.
    
#### 3. Unordered Associative Containers (since C++11)
These containers store elements in no specific order but provide fast access based on their value or key.

- **`std::unordered_set`**: An unordered collection of unique elements.
    
- **`std::unordered_multiset`**: Allows duplicate elements in an unordered collection.
    
- **`std::unordered_map`**: An unordered collection of key-value pairs with unique keys.
    
- **`std::unordered_multimap`**: Allows keys to have multiple values in an unordered collection.
    
#### 4. Container Adaptors
These adapt sequence containers to provide a different interface.

- **`std::stack`**: Adapts a container to provide stack (LIFO - Last In, First Out) operations.
    
- **`std::queue`**: Adapts a container to provide queue (FIFO - First In, First Out) operations.
    
- **`std::priority_queue`**: Like a queue, but elements are removed based on their priority.