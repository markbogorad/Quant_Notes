up:: [[Data MOC]]
tags:: #Programming 
# MapReduce
- Programming framework of processing large datasets in parallel across many machines
- **Map:** distribute a computational problem across a cluster
- **Reduce:** Master node collects the answers to all the sub-problems and combines them
## [[Big Data]] Framework
![[Pasted image 20250507124639.png]]
![[Pasted image 20250507124644.png]]
- Critical aspects: fault tolerance + replication + load balancing, monitoring
	- At any point, 1/1000 systems are going to be down which needs to be the norm

## Coding Perspective
- ![[Pasted image 20250508073602.png]]
- Mapping is converting the input data into key-value pairs 
- Reducing is matching the bits after mapped