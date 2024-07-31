### Transient Analysis:
Transient analysis is concerned with the computation of the probabilities $P(X(t) = j)$.

##### Vector of the state probabilities at time $t$
Let's define the **vector of the state probabilities at time $t$** as:
$$
\Pi(t) \triangleq \left[ \Pi_1(t), \ \Pi_2(t), \ \Pi_3(t), \ \ldots \right]
$$
where:
$$
\Pi_j(t) = P(X(t) = j)\ ,  \kern 30px j = 1, \ 2, \ 3, \ \ldots
$$
Then we have, using the [[DES - Theorem 'Total Probability Rule'|total probability rule]]:
$$
\Pi_j(t) = \sum_{\atop \LARGE i \in \mathcal{X}} \underbrace{P(X(t) = j \mid X(0) = i)}_{\atop \LARGE p_{i,j}(t)} \cdot \underbrace{P(X(0) = i)}_{\atop \LARGE \Pi_i(0)}
$$

###### In Matrix Form:
$$
\Pi(t) = \Pi(0)\cdot H(t)
$$
Then using a [[DES - Definition of 'Transition Rate Matrix Q'#Relation with the matrix H t|property]] of the matrix $Q$, we can write:
$$
\Pi(t) = \Pi(0) \cdot e^{Qt}
$$
---
### Observation:
$$
\frac{d}{dt}\Pi(t) = \frac{d}{dt}\left( \Pi(0) \cdot e^{Qt} \right)
$$
Hence, $\Pi(t)$ is the solution of the Cauchy problem.

---
###### ~Example: 
