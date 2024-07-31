### Limit Probability:
Let:
$$
\Pi_i \triangleq \lim_{t \, \to \, + \infty} \Pi_i(t)
$$
Where:
$$
\Pi_i(t) \triangleq P(X(i) = i)
$$
If the limit exists, $\Pi_i$ is called **limit probability** of state $i$.
If the limit probabilities exist for all states $i \in \mathcal{X}$,then the row vector
$$
\Pi \triangleq \left[\Pi_1, \ \Pi_2, \ \Pi_3, \ \ldots \right]
$$
Is called **limit state probability vector**.

###### Properties of the Limit State Probability Vector:
$i$) Existence

$ii$) Uniqueness
- There exist only one $\Pi$ such that: $\Pi \triangleq \lim_{t \, \to \, + \infty} \Pi(t)$

$iii$) Consistency
- $\sum_{i} \Pi_i = 1$

Which are given by this [[DES - Theorem of 'Existence, Uniqueness and Consistency of the Limit State Probability Vector'|Theorem]].

---
###### ~Example: