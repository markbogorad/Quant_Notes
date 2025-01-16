up:: [[Computer Science MOC]]
tags:: #Programming  
# Priority Queue
- Abstract [[Data Types]] where elements have a priority, and higher priority elements are served first
## Heap
- Most common type is the heap:
	- Min Heap: smallest element at the root
	- Max Heap: largest element a the root
- With heaps, only the root is sorted, the rest is unsorted, resulting in high [[Program Running Time (Big O)]]
- Inserting heap elements
	- Find a spot on the bottom nodes, compare if the element takes higher priority, if so, move it up a level of nodes, and repeat until it is in it's correct place
- Can be represented with [[Arrays]]
- 