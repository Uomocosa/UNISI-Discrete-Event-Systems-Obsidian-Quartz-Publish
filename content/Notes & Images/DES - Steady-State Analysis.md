### Steady-State Analysis:
In [[DES - Transient Analysis|transient analysis]] we compute the probabilities:
$$
\Pi_i(t) \triangleq P(X(i) = i)
$$
Next we will address the computation of the limits of these probabilities for $t \to \infty$ :
$$
\Pi_i \triangleq \lim_{t \, \to \, + \infty} \Pi_i(t)
$$
This is the topic of **steady-state analysis**

###### Motivation
Drop the dependence of state probabilities on the time $t$, and work with constant probabilities (the limits) instead of time-varying ones.
![[Pasted image 20220125165237.png]]

---
### Classification of the States
For the purpose of steady-state analysis, we first need to introduce the [[DES - Classification of the States of a CTHMC|classification of the states of a CTHMC]].

---
### Recurrent Time of State $i$ ($T_{i,i}$):
Then, we introduce the following random variable $T_{i,i}$

![[Pasted image 20220125172621.png]]

$T_{i,i}$ is called **recurrent time** of state $i$.
$T_{i,i}$ is a continuous random variable, described by:
$$
\Phi_i(t) \triangleq P(T_{i,i} \le t), \kern 15px t \ge 0
$$
---
###### Limit of the CDF: $p_i$
Let:
$$
p_i \triangleq \lim_{t \ \to \ \infty} \Phi_i(t)
$$
![[Pasted image 20220125172951.png]]

Where $p_i$ is the probability that the system returns to the state $i$ in the future.
$\Rightarrow$ $1 - p_i$ is the probability that the system **does not** return to the state $i$ in the future.

It turns out that:
- If $p_i = 1$, state $i$ is [[DES - Definition of 'Recurrent State or Transient State'|recurrent]]
- If $p_i < 1$, state $i$ is [[DES - Definition of 'Recurrent State or Transient State'|transient]]

Now assume $p_i = 1 \kern 10px \Rightarrow \kern 10px \Phi_i(t)$ is the [[DES - (CDF) Cumulative Distribution Function|cdf]] of $T_{i,i}$.

Let:
$$
\varphi_i(t) \triangleq \frac{d}{dt}\Phi_i(t)
$$
Then: $\varphi_i$ is the [[DES - (PDF) Probability Distribution Function|pdf]] of $T_{i,i}$

---
###### Expected Value of $T_{i,i}$:
Now if we compute [[DES - Definition of 'Expected Value'|expected value]] of $T_{i,i}$:
$$
M_i \triangleq \int_{0}^{+ \ \infty} t \ \varphi_i(t) \ dt
$$
- If $M_i < + \infty$, state $i$ is **positive recurrent**
- If $M_i = + \infty$, state $i$ is **null recurrent**

Where for **positive recurrent** state $i$, we expect $\Pi_i > 0$
While for **null recurrent** state $i$, we expect $\Pi_i = 0$

---
###### ~Example: 
![[Pasted image 20220125174934.png]]

- If $\lambda > \mu$ then the state number goes to infinity as time goes on. 
- If $\lambda < \mu$ then the most visited state is the first, the second has been visited less the the first, and so on, $\Pi$ assume defined values.
- If $\lambda = \mu$ as the time increases at infinity all the states could have been visited the same number of times, $\Pi$ is a vector of all zeros.

---
###### Results:
- If $\mathcal{X}$ is finite, then at least one state is **recurrent**.
- If $i \in \mathcal{X}$ is **positive recurrent**, and $j \in \mathcal{X}$ is **reachable** from $i$, then also $j$ is **positive recurrent**.
- If $S \subseteq \mathcal{X}$ is **closed** and **irreducible**, then one of the following holds:
	- all states in $S$ are **positive recurrent**
	- all states in $S$ are **null recurrent**
	- all states in $S$ are **transient**

This means that it is sufficient to classify a single state from the system, then the others are classified accordingly.

- If $S \subseteq \mathcal{X}$ is **closed** and **irreducible** and **finite**, then all states in $S$ are **positive recurrent**

---
