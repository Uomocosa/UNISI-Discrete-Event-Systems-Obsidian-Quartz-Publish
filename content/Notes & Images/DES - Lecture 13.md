###### Recap Stochastic Timed Automaton with Poisson Clock Structure
Given a [[DES - Definition of 'Stochastic Timed Automata'|stochastic timed automaton]] $\left(\mathcal{E}, \mathcal{X}, \Gamma, p, p_{x_{0}}, F\right)$, so far we mostly focused on computing:
$$
\begin{align}
&p_{E_k}(e) \triangleq P(E_k = e)
\\[5px]
&p_{X_k}(x) \triangleq P(X_k = x)
\end{align}
$$
Where $k$ is the **event index**

In particular, for [[DES - Model of a Stochastic Timed Automata with Poisson Clock Structure|stochastic timed automata with Poisson clock structure]], computing these probabilities only requires simple matrix computations:
$$
\begin{align}
&\Pi_{E}(k) = \Pi_{X}(0) \cdot P_{x}^{k-1} \cdot P_E
\\[5px]
&\Pi_{X}(k) = \Pi_{X}(0) \cdot P_{x}^{k}
\end{align}
$$
---
# Introduction:
Now our focus moves on computing:
$$
P(X(t) = x)
$$
Where $X(T)$ is the random variable describing the **state** of the system at time $t$
> What is the probability that at time $t$ the state will be $x$

---
# Arguments:
- [[DES - Definition of 'Stochastic Process']]
- [[DES - Definition of 'Chain']]
- [[DES - Definition of 'Homogeneity']]
- [[DES - Definition of 'Independent Stochastic Process']]
- [[DES - Definition of 'Markov Process']]
- [[DES - Definition of 'Continuous Time Homogeneous Markov Chain (CTHMC)']]
- [[DES - Definition of 'Transition Function Matrix for CTHMC']]
- [[DES - Chapman-Kolmogorov Equation]]
- [[DES - Definition of 'Transition Rate Matrix Q']]
- [[DES - Demonstration on How to Calculate the Transition Rate Matrix Q]]
- [[DES - Graphical Representation of CTHMC]]
- [[DES - Transient Analysis]]
- [[DES - Steady-State Analysis]]
	- [[DES - Classification of the States of a CTHMC]]
- [[DES - Definition of 'Limit State Probability Vector']]
	- [[DES - Theorem of 'Existence, Uniqueness and Consistency of the Limit State Probability Vector']]
		- [[DES - Definition of 'Irreducible CTHMC']]