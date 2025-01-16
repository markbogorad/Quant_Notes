up:: [[Computer Science MOC]]
tags:: #Programming  
# Search Trees
## Binary Tree
- Similar node structure to that of a [[Linked Lists]]
	- Except each node points to 2 other nodes, creating a binomial tree
## Binary Search Tree
- A binary tree except the left node must be smaller and the right node must be greater or equal
	- Perfect for a Binary Search [[Linear Search]] using halving


![[1*tUBYCHi32Zj0B2UCw0qmlA.png]]

## Implementing:
- ![[Pasted image 20240707121645.png]]
# Search Tree Traversal
## Depth First Search
- Goes all the way down one path in a [[Search Trees]] and then onto a 2nd one
	- **Essentially printing a stack here
- Uses a [[Stack]]
	- In pseudocode:
		- Initialize stack and add root
		- While there are elements still in the stack
			- Pop the stack
			- Print that element
			- Add children to stack
## Breadth First Search
- Scans [[Search Trees]] level by level
	- **Essentially printing a queue here**
- Uses a [[Queue]]
	- Pop from beginning of list instead of end
	- Allows trees to print in levels