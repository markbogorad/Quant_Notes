up:: [[Data MOC]]
tags:: #Programming 
# Parallelism
- The system actually executes multiple tasks at the exact same time, typically using multiple cores or processors

|Concept|Key Idea|Simultaneity?|Example Use Case|
|---|---|---|---|
|**Multithreading**|Multiple threads in one process|Not necessarily|UI + background task|
|**Concurrency**|Multiple tasks logically at once|Not necessarily|Database handling many queries|
|**Parallelism**|Multiple tasks physically at once|Yes|MapReduce processing stock data|

- **Multithreading**: One person juggling 3 balls.
- **Concurrency**: One cook making several dishes by switching tasks efficiently.
- **Parallelism**: Several cooks making dishes at the same time in different kitchens.