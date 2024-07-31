###### Arguments:
- [[DES - Exponential Distribution]]
- [[DES - Definition of 'Memory-Less Property']]

---
Demonstration that the exponential distribution enjoys the memory-less property:

From the definition of **conditional probability** we have:
$$
P(A \mid B) = \frac{P(A \cap B)}{P(B)}
$$
Where $P(A \cap B)$ is usually wrote as: $P(A, B)$

![[Pasted image 20220122163615.png]]

We can that $P(X > t+s | X > t) = P(X > t+s)$ because logically if $X > t+s$ is obvious that it will be $X > t$, (as $s$ is $\ge 0$).