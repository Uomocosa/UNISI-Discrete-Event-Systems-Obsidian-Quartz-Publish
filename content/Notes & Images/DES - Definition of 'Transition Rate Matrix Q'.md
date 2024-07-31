### Transition Rate Matrix Q:
Let:
$$
Q \triangleq \lim_{dt \to 0} \frac{H(dt) - I}{dt}
$$
Matrix $Q$ is called **transition rate matrix**, because its entries have the dimension of $\left[\text{time}^{-1}\right]$

The entry of $Q$ in position $(i,j)$ will be denoted $q_{i,j}$
$$
Q \triangleq \left[q_{i,j}\right]_{i,j \in \mathcal{X}}
= \left[
\begin{array}{cccc}
q_{1,1} & q_{1,2} & q_{1,3} & \ldots
\\
q_{2,1} & q_{2,2} & q_{2,3} & \ldots
\\
q_{2,1} & q_{3,2} & q_{3,3} & \ldots
\\
\vdots & \vdots  & \vdots  & \ddots
\end{array}
\right]
$$
###### Properties of $Q$
1. The entries $q_{i,j}$ of $Q$ are **nonnegative** for $j \neq i$. [[DES - Demonstration of the First Property of the Transition Rate Matrix Q|Demonstration]].
2. The sum along any row of $Q$ is $0$, it can be also said that: $Q \cdot \vec{\mathbb{1}}  = 0$ [[DES - Demonstration of the Second Property of the Transition Rate Matrix Q|Demonstration]].
3. The entries $q_{i,i}$ of $Q$ are **nonpositive** for $j \neq i$. [[DES - Demonstration of the Third Property of the Transition Rate Matrix Q|Demonstration]].

###### Relation with the matrix $H(t)$

^cb5882

[[DES - Definition of 'Transition Function Matrix for CTHMC'|Definition]] of the **Transition Function Matrix**: $H(t)$
1.
$$
\frac{d}{dt}H(t) = H(t) \cdot Q
$$
2.
$$
H(t) = e^{Q t}
$$
3.
$$
p_{i,j} = - \frac{q_{i,j}}{q_{i,i}}
$$

###### Relation with the mean State Holding Time $\operatorname{E}\left[V(i)\right]$
[[DES - Definition of 'State Holding Time']] of the **State Holding Time**: $V(i)$
1.
$$
q_{i,i} = - \frac{1}{E\left[V(i)\right]}
$$
---
##### Demonstration on How to Calculate the Transition Rate Matrix $Q$
[[DES - Demonstration on How to Calculate the Transition Rate Matrix Q]]

---
###### ~Example: Relation of $Q$ with the Graphical Representation
![[Pasted image 20220125152502.png]]