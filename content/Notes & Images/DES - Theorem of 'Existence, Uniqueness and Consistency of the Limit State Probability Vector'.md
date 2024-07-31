### Theorem: Existence, Uniqueness and Consistency of the Limit State Probability Vector:
Let ($\mathcal{X}, Q, \Pi_0$) be an [[DES - Definition of 'Irreducible CTHMC'|irreducible CTHMC]] with all [[DES - Steady-State Analysis#Expected Value of T_ i i|positive recurrent]] states.
Then, there **exists** an **unique** [[DES - Definition of 'Limit State Probability Vector'|limit probability vector]]:
$$
\Pi \triangleq \left[\Pi_1, \ \Pi_2, \ \Pi_3, \ \ldots \right]
$$
The vector $\Pi$ is such that:
$$
\Pi_i > 0 \kern 15px \forall \ i \in \mathcal{X}
$$
and the limit probability vector is also **consistent**
$$
\sum_{\atop \LARGE i \in \mathcal{X}} \Pi_i = 1
$$
###### Analytic Solutions of $\Pi$
Moreover, $\Pi$ can be computed by solving the following linear system of equations:
$$
\left\{
\begin{align}
	&\kern 7px \Pi \cdot Q = 0
	\\[5px]
	&\sum_{\atop \LARGE i \in \mathcal{X}} \Pi_i = 1
\end{align}
\right.
$$
---
### Corollary:
The theorem above also holds if ($\mathcal{X}, Q, \Pi_0$) is an [[DES - Definition of 'Irreducible CTHMC'|irreducible CTHMC]]  and the number of states is **finite**

---
### Observation:
Recall that $\Pi(t)$ satisfies the differential equation:
$$
\frac{d}{dt}\Pi(t) = \Pi(t) \cdot Q
$$
Then we can say:
$$
\begin{align}
&\text{If } \ \ \Pi(t) \to \Pi, \ \ \text{with: }\Pi\text{ cosntant}
\\[5px]
& \text{then: } \ \ \frac{d}{dt}\Pi(t) \to 0
\\[5px]
& \text{hence: } \ \ \Pi \cdot Q = 0


\end{align}
$$
---
### Observation:
$\Pi \cdot Q = 0$ is a square system, with $Q$ as **singular** matrix, so it is **non-invertible**.

> $Q$ is **singular** because: in the [[DES - Definition of 'Transition Rate Matrix Q'#Properties of Q|properties of the matrix Q]] is shown that $Q \cdot \vec{\mathbb{1}}  = 0$.
> The definition of a **singular matrix**

So $\Pi \cdot Q = 0$ has an infinite number of solutions, in order to select **the only one** that represent a [[DES - (PMF) Probability Mass Function|pmf]], we add the constraint of **consistency**: $\sum_{\atop \LARGE i \in \mathcal{X}} \Pi_i = 1$

---
###### ~Example:
![[13 - Continuous-time homogeneous Markov chains(36-37)_211218_153102.pdf]]

---