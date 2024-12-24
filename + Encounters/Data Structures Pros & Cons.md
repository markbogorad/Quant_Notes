up:: [[Computer Science MOC]]
tags:: #Programming  

| Data Structure / Algorithm | Purpose | Computing Speed | Pros | Cons |
|----------------------------|---------|-----------------|------|------|
| **Linear Search** | Find an element in a list | O(n) | Simple to implement, does not require sorted data | Slow for large datasets |
| **Binary Search** | Find an element in a sorted list | O(log n) | Efficient for large datasets, faster than linear search | Requires sorted data |
| **Sorting Algorithms** | Arrange elements in a specific order | Varies (O(n log n) for efficient sorts like Merge Sort, Quick Sort) | Organizes data for efficient searching and processing | Can be complex, some have high space complexity |
| **Search Trees** | Maintain a dynamic set of elements, support queries and updates | O(log n) for balanced trees (e.g., AVL, Red-Black) | Supports dynamic sets, efficient search, insertion, deletion | Balancing can be complex, unbalanced trees have poor performance |
| **Tries** | Store a dynamic set of strings, often for quick prefix queries | O(L) where L is the length of the string | Efficient for prefix-based queries, fast lookup | High space complexity, complex implementation |
| **Stack** | Last In, First Out (LIFO) data structure | O(1) for push/pop operations | Simple to implement, efficient | Limited access to only the top element |
| **Queue** | First In, First Out (FIFO) data structure | O(1) for enqueue/dequeue operations | Simple to implement, efficient | Limited access to only the front and rear elements |
| **Priority Queue** | Elements are processed based on priority | O(log n) for insertion and deletion | Efficient for scheduling tasks, Dijkstra’s algorithm | Higher complexity compared to regular queues |
| **Graphs** | Represent relationships between entities | Varies (O(V+E) for traversal algorithms) | Models complex relationships, supports various algorithms (e.g., DFS, BFS) | Can be complex to implement and manage, high space complexity |
| **Hash Tables** | Store key-value pairs with fast retrieval | O(1) average for insert, delete, search | Fast lookup, insertion, and deletion | Poor performance with many collisions, hash function complexity |
| **Dictionaries** | Store key-value pairs, similar to hash tables | O(1) average for insert, delete, search | High-level abstraction, easy to use in programming languages | Similar cons as hash tables, may have overhead in certain languages |

### Detailed Descriptions

1. [[Linear Search]]
   - **Purpose:** Simple search for an element in a list.
   - **Computing Speed:** O(n) where n is the number of elements.
   - **Pros:** Easy to implement; works with unsorted data.
   - **Cons:** Inefficient for large datasets; slow compared to other search algorithms.

2. [[Binary Search]]
   - **Purpose:** Efficient search for an element in a sorted list.
   - **Computing Speed:** O(log n) where n is the number of elements.
   - **Pros:** Much faster than linear search for large datasets.
   - **Cons:** Requires the data to be sorted beforehand.

3. [[Sorting Algorithms]]
   - **Purpose:** Arrange elements in a specific order (ascending or descending).
   - **Computing Speed:** Varies; efficient sorts like Merge Sort and Quick Sort have O(n log n).
   - **Pros:** Organizes data for efficient searching and processing.
   - **Cons:** Some sorting algorithms can be complex and have high space complexity.

4. [[Search Trees]]
   - **Purpose:** Maintain a dynamic set of elements supporting queries and updates.
   - **Computing Speed:** O(log n) for balanced trees.
   - **Pros:** Efficient for search, insertion, and deletion.
   - **Cons:** Balancing trees can be complex; unbalanced trees degrade performance.

5. [[Tries]]
   - **Purpose:** Store a dynamic set of strings for quick prefix-based queries.
   - **Computing Speed:** O(L) where L is the length of the string.
   - **Pros:** Fast lookups; efficient for prefix queries.
   - **Cons:** High space complexity; complex implementation.

6. [[Stack]]
   - **Purpose:** LIFO data structure for temporary storage and retrieval.
   - **Computing Speed:** O(1) for push and pop operations.
   - **Pros:** Simple and efficient; used in function call management.
   - **Cons:** Limited to accessing the top element only.

7. [[Queue]]
   - **Purpose:** FIFO data structure for temporary storage and retrieval.
   - **Computing Speed:** O(1) for enqueue and dequeue operations.
   - **Pros:** Simple and efficient; used in task scheduling and buffering.
   - **Cons:** Limited to accessing the front and rear elements only.

8. [[Priority Queue]]
   - **Purpose:** Process elements based on priority.
   - **Computing Speed:** O(log n) for insertion and deletion.
   - **Pros:** Efficient for scheduling and algorithms like Dijkstra's.
   - **Cons:** Higher complexity than regular queues.

9. [[Graphs (Data Structure)]]
   - **Purpose:** Represent relationships between entities (nodes and edges).
   - **Computing Speed:** Varies; traversal algorithms like DFS and BFS are O(V+E).
   - **Pros:** Models complex relationships; supports many algorithms.
   - **Cons:** Can be complex; high space complexity.

10. [[Hash Tables]]
    - **Purpose:** Store key-value pairs with fast retrieval.
    - **Computing Speed:** O(1) on average for insert, delete, and search.
    - **Pros:** Very fast lookup and modification.
    - **Cons:** Poor performance with many collisions; complexity of hash functions.

11. [[Dictionaries]]
    - **Purpose:** Store key-value pairs (similar to hash tables).
    - **Computing Speed:** O(1) on average for insert, delete, and search.
    - **Pros:** Easy to use; high-level abstraction in many languages.
    - **Cons:** Similar to hash tables; may have overhead.
