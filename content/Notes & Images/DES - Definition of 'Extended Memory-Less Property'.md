### Extended Memory-Less Property:
Let $X$, $Y$ be independent variables such that:
- $X \sim Exp\left(\frac{1}{\lambda}\right)$
- $f_Y(y) = 0 \kern 10px \text{for} \kern 10px y \le 0$
	- where: $f_Y$ denotes the [[DES - (PDF) Probability Distribution Function|pdf]] of $Y$.
- Moreover, let $s \ge 0$.

Then the Extended Memory-Less Property enunciate that:
$$
P(X > Y + s \mid X > Y) = P(X > s)
$$
And using the probability of the complement of an event:
$$
P(X \le Y + s \mid X > Y) = P(X \le s)
$$
---
### Demonstration
[[DES - Demonstration of the Extended Memory-Less Property]]

---