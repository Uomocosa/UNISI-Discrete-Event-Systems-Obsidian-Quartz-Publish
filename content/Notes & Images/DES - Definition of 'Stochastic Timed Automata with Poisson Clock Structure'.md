### Stochastic Timed Automata with Poisson Clock Structure:
Given a [[DES - Definition of 'Stochastic Timed Automata'|stochastic timed automata]] we define it as having a [[DES - Definition of 'Poisson Clock Structure'|Poisson clock structure]] if we have that **all** [[DES - Definition of 'State Holding Time'|state holding times]] $\left\{V(x_1), \ V(x_2), \ V(x_3), \ \ldots \right\}$ have a [[DES - Exponential Distribution|exponential distribution]], so that:
$$
V(x_i) \sim \operatorname{Exp}\left(\frac{1}{\lambda_i}\right)
$$
Often you see $V(i)$ instead of $V(x_i)$, but they mean the same thing.

---
###### ~Example: