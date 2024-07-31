###### Summary:
We demonstrate that given a *Timed Automata with Poisson Clock Structure* the vector of all **State Holding Time** has an **exponential distribution**, with rate:
$$
\sum_{e \in \Gamma(x)} \lambda_e \ p(x' \mid x, e) \kern 30px \text{for} \ \ x' \neq x
$$
Where $p(x' \mid x, e)$ is the probability of changing state from state $x$ when event $e$ occurs, and $\lambda_e$ is the **rate** of the exponential distribution that generated event $e$.

And the **average state holding time** is:
$$
\operatorname{E}\left[V(i)\right] = \frac{1}{\sum \lambda_e \ p(x' \mid x, e)}
$$

---
### Theorem: Distribution of the State Holding Time for a Poisson Clock Structure
We want to compute the **distribution** of the [[DES - Definition of 'State Holding Time'|State Holding Time]] $V(x)$ for a stochastic timed automaton with [[DES - Definition of 'Poisson Clock Structure'|Poisson Clock Structure]].

*==Preliminary result==*:
Let $X_{1}, X_{2}, \ldots, X_{n}, X_{n+1}$ be independent, identically distributed random variables with $X_{i} \sim \operatorname{Exp}\left(\frac{1}{\lambda}\right)$ for all $i=1,2, \ldots, n+1$. Then, for $t>0$ :
$$
P\left(X_{1}+\ldots+X_{n}<t, \; X_{1}+\ldots+X_{n}+X_{n+1}>t\right)=\frac{(\lambda t)^{n}}{n !} e^{-\lambda t}
$$
The preliminary result can be found knowing the result from the [[DES - Definition of a 'Poisson Process'|Poisson Process]] and the [[DES - Definition of 'Memory-Less Property'|memory-less property]] of the exponential distribution.

[[DES - Demonstration of the State Holding Time for a Poisson Clock Structure]]

---
##### ~Example:
![[Pasted image 20220128180010.png]]

---
