### Arguments
- [[DES - Definition of 'Transition Function Matrix for CTHMC'#^bc4308|Definition]] of $p_{i,j}(t)$
- [[DES - Theorem 'Total Probability Rule']]
- [[DES - Definition of 'Markov Process']]
- [[DES - Chapman-Kolmogorov Equation]]

---
###### Summary
Starting from:
$$
p_{i,j} \triangleq P(X(s+t) = j \mid X(s) = i)
$$
We want to arrive at:
$$
p_{i,j} = \sum_{r \in \mathcal{X}} P(X(s+t) = j \mid X(s+u) = r) \cdot P(X(s+u) = r \mid X(s) = i)
$$

---
![[Pasted image 20220128212125.png]]

In matrix form this is equal to say:
$$
H(t) = H(u) \cdot H(t-u)
$$