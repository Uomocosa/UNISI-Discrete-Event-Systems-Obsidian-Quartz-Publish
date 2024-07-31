###### Summary
The probability that we are at state $A$ is equal to the **sum** of all probabilities that the events $B_i$ brings us to state $A$ multiplied by the probability that event $B_i$ has to happen.

---
### Total Probability Rule

Let $\Omega$ be the set of all possible outcomes of a random experiment (also called the sample space)
Let $A$ be an event (i.e., a subset of $\Omega$ ), and $B_{1}, \ldots, B_{n}$ be a partition of $\Omega$ :
- $B_{1}, \ldots, B_{n}$ are events
- $B_{1} \cup \ldots \cup B_{n}=\Omega$:
- $B_i \cap{} B_j = \varnothing$; for all $i \neq j$

Then:
$$
P(A)=\sum_{i=1}^{n} P\left(A \mid B_{i}\right) \cdot{} P\left(B_{i}\right)
$$
If $C$ is another event, we also have:
$$
P(A \mid C)=\sum_{i=1}^{n} P\left(A \mid B_{i}\,,C\right) \cdot{} P\left(B_{i} \mid C\right)
$$

---
###### Observation:
Usually we use this theorem because computing the probability of the sum is much easier than directly computing $P(A)$ or $P(A \mid C)$ directly.
Practically we get to use the additional information provided by $B_i$

---
###### ~Example:
![[Pasted image 20220120090114.png]]