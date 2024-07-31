### Superposition:
Let $X_1$, $X_2$, ..., $X_n$ be independent random variables, each having an [[DES - Exponential Distribution|exponential distribution]]:
$$
X_i \sim Exp\left(\frac{1}{\lambda_i}\right) \kern 30px i = 1, 2, ..., n
$$

Define the **superposition** of $X_1$, $X_2$, ..., $X_n$ as
$$
X = \min _{i = 1, \,...,\, n} X_i
$$
Also we have that the superposition in characterised by an exponential distribution of rate $\Lambda$, where:
$$
\Lambda = \sum_{i=1}^n X_i
$$
- [[DES - Demonstration of the Exponential Distribution of the Superposition|Demonstration]]

---
###### ~Example: Why is the superposition useful?
Suppose we have a [[DES - Definition of 'Poisson Clock Structure'|Poisson Clock Structure]] with two events $X$ and $Y$ declared as:
$$
\begin{align}
X \sim Exp\left(\frac{1}{\lambda}\right)
\\[5px]
Y \sim Exp\left(\frac{1}{\mu}\right)
\end{align}
$$
Then the following equations holds:
$$
\begin{align}
P(X < Y + t) = & \space 1 - \frac{\mu}{\lambda + \mu}e^{-\lambda t} & , \space t \ge 0
\\
= & \space \frac{\lambda}{\lambda + \mu}e^{-\lambda t} & , \space  t \ge 0
\end{align}
$$
- [[DES - Demonstration on How to Use the Superposition|Demonstration]]

And for $t = 0$: 
$$
P(X < Y) = \frac{\lambda}{\Lambda}
$$
Where: $\Lambda$ is the **rate** of the distribution of the superposition, which is defined in this case as:
$$
\Lambda = \lambda + \mu
$$

---