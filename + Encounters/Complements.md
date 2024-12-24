up:: [[Probability MOC]]
tags:: #Math
# Complement Rules
- [[De Morgan's Laws]]
	- * not distributive, union becomes intersection
	- $(A \cup B)^c = A^c \cap B^c$
	- $(A \cap B)^c = A^c \cup B^c$
- Probability of the union of 2 events = 1 - probability of the complements of their intersection
	- $P(A∪B)=1−P(A^c∩B^c)$
		- And
	- $P(A^c∩B^c)=1−P(A∪B)$
- [[Law of Total Probability]]
	- $P(A^c) = \sum_{i=1}^{n} P(A^c|B_i)P(B_i)$
		- same as: $P(A)=P(A∣B) P(B)+P(A∣B^c) P(B^c)$
- [[Bayes Theorem]]
	- $P(Bi​∣A^c)=\frac{P(A^c∣Bi​)P(Bi)}{P(A^c)}​$
	- 