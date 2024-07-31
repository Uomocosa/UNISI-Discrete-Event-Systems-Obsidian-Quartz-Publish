###### Summary:
The Transition Function Matrix $H(t)$ supports this formula:
$$
H(t) = H(u)\cdot H(t-u) \kern 30px 0 \le u \le t
$$
---
### Chapman-Kolmogorov Equation:
Knowing that, from the definition:
$$
p_{i,j}(t) \triangleq P(X(s+t) = j \mid X(s) = i)
$$
We can say, knowing the [[DES - Theorem 'Total Probability Rule'|Total Probability Rule]] that:
$$
p_{i,j}(t) = \sum_{\atop \Large r \in \mathcal{X}}
p_{i,r}(u) \cdot p_{r,j}(t-u)
$$
Where:
$$
p_{i,r}(u) = P(\textcolor{orange}{X(s+u) = r} \mid X(s) = i)
$$
And,
$$
p_{r,j}(t-u) = P(X(s+t) = j \mid \textcolor{orange}{X(s+u) = r})
$$

With the notion of how the matrix $H(t)$ is [[DES - Definition of 'Transition Function Matrix for CTHMC'#^2d24e9|defined]] we can say that:
- $p_{i,j}(t)$ is the entry in position $(i,j)$ of the matrix $H(t)$
- $p_{i,r}(u)$ is the entry in position $(i,r)$ of the matrix $H(u)$
- $p_{r,j}(u)$ is the entry in position $(r,j)$ of the matrix $H(t-u)$

> So $p_{i,j}(t)$ is the product of the $i$-th row of $H(u)$ and the $j$-th row of $H(t-u)$

###### Matrix Form of the Chapman-Kolmogorov Equation
So the Chapman-Kolmogorov Equation can be rewritten in **matrix form**:
$$
H(t) = H(u)\cdot H(t-u) \kern 30px 0 \le u \le t
$$
---
###### Demonstration:
[[DES - Demonstration of the Chapman-Kolmogorov Equation]]

---
###### ~Example: