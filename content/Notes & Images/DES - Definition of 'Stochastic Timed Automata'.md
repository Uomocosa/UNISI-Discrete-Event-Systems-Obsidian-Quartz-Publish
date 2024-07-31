### Stochastic Timed Automaton:
A stochastic timed automaton is a 6-tuple $\left(\mathcal{E}, \ \mathcal{X}, \ \Gamma, \ p, \ p_{x_{0}}, \ F\right)$,where:
- $\mathcal{E}$ is a discrete **set of events**.
- $\mathcal{X}$ is a discrete **set of states**.
- For each $x \in \mathcal{X}$, $\Gamma(x) \subseteq \mathcal{E}$ is the set of events that are possible in state $x$.
- For each $x',  x \in \mathcal{X}$ and $e \in \Gamma$, $p(x' \mid x, e)$ is the probability that the next state is $x'$, given the current state $x$ and the next event $e$.
> **NOTE**: 
> When we talk about next event immagine always that at state 0: $x_0$ the next event **to finish** is event $e_1$, also that event $e_0$ does not exist.
> 
> Then to give a general rule: at state $x_3$ event $e_3$ has already occurred, and the next event to occur will be $e_4$. 
-  $F = \left\{F_e : e \in \mathcal{E}\right\}$ is a **stochastic clock structure**.

---

###### ~Example: 


---
#### Observation $\mathrm{I}\,$:
[[DES - Definition of 'Timed Automata'|Timed Automata]] are a special case of **Stochastic Timed Automata**, where all probability $p(x' \mid x, e)$ = 1, which means that all conditional probability are certain.
And $p_{x_0}(x) = 1 \space \Longleftrightarrow \space x = x_0$.

---
#### Observation $\mathrm{II}\,$:
There could also exist **mixed timed automata**, where only the clock structure is stochastic ($f\,$, $x_0\,$, $F\,$), one where the transition function and the initial state are stochastic:  ($p\,$, $p_{x_0}\,$, $V\,$), and all other possible combinations.
> **TERMINOLOGY**
> $p$ is defined as **probability mass function** (pmf)
	> $p_{x_0}$ is defined as **pmf of the initial state**.
	> $p_{E_1}$ is defined as **pmf of the first event**.
	> $p_{X_5}$ is defined as **pmf of the fifth state**.

