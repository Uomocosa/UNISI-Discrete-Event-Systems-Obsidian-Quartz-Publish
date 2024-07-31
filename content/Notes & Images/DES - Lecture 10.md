A stochastic timed automaton $\left(\varepsilon, x, \Gamma, p, p_{x_{0}}, F\right)$ transforms the stochastic clock structure $F$ into the pmf's of the event and state sequences:

$$
F \longrightarrow \begin{gathered}
\text { Stochastic } \\
\text { timed } \\
\text { automaton }
\end{gathered} \longrightarrow P_{E_{1},} P_{E_{2},}, P_{E_{3}, \ldots}
$$

The basic brick to carry out this task, is the computation of probabilities of the type:
$$
P\left(E_{k}=e \mid X_{k-1}=x\right)
$$
> "Probability of event $e$ at state $x$"

Indeed, if these probabilities are known, then, using the total probability rule:
- $P\left(E_{k}=e\right)=\sum_{x \in X} \left( P\left(E_{k}=e \mid X_{k-1}=x\right) \cdot P\left(X_{k-1}=x\right)\right)$
- $P\left(X_{k}=x^{\prime}\right)=\sum_{x \in X} \left( P\left(X_{k}=x^{\prime} \mid X_{k-1}=x\right) \cdot P\left(X_{k-1}=x\right)\right)$

Then:
$$
P\left(X_{k}=x^{\prime} \mid X_{k-1}=x\right)=
\sum_{e \in \Gamma(x)}
\underbrace{
P\left(X_{k}=x^{\prime} \mid X_{k-1}=x, E_{k}=e\right)
}_{\LARGE p\left(x^{\prime} \mid x, e\right)}
\:
P\left(E_{k}=e \mid X_{k-1}=x\right)
$$

$\Rightarrow$ So starting from $p_{x_0}$ (pmf of the initial state) we can find all the pmf of the events: $\left\{p_{x_1}, \space p_{x_2}, \space ..., \space p_{x_n}\right\}$ and all the pmf of the events: $\left\{p_{E_1}, \space p_{E_2}, \space ..., \space p_{E_n}\right\}$
- Given $p_{x_{0}}$, we compute $p_{E_{1}}$ and $p_{x_{1}}$. 
- Then, given $p_{x_{1}}$, we compute $p_{E_{2}}$ and $p_{x_{2}}$. 
And so on... $\Rightarrow$ **iterative approach** 

---
Formally,
$$
P\left(E_{k}=e \mid X_{k-1}=x\right)=P\left(Y_{e, k-1}<\min _{e^{\prime} \in \Gamma(x) \atop e^{\prime} \neq e} Y_{e^{\prime}, k-1}\right)
$$
- Where: $Y_{a}$ is the **residual lifetime** of event a
- The formula above states that the probability of event e at state x to occur is equal to the probability that the residual lifetime of event e at state x is the **lowest** out of all the other residual lifetimes.

Unfortunately, the distributions of the residual lifetimes are unknown in general, if we only assume the knowledge of the current state. 
Hence, $P\left(E_{k}=e \mid X_{k-1}=x\right)$ cannot be computed easily.

For this reason, in the exercises we had to consider all the possible cases, starting from initialization, which results into a dramatic proliferation of cases as the event index increases.

The question now is whether there exist classes of stochastic timed automata for which computing $P\left(E_{k}=e \mid X_{k-1}=x\right)$ is an easy task.

The answer is given by stochastic timed automata with **Poisson clock structure**.

> **MAIN RESULT**:
> For a stochastic timed automata with [[DES - Definition of 'Poisson Clock Structure'|Poisson Clock Structure]], the residual lifetime of an event has the same distribution as the **total lifetime**.
> 
> Thanks to the [[DES - Definition of 'Memory-Less Property'|memory-less property]] of [[DES - Exponential Distribution|exponential distribution]] we do not care about the past of a single event (whether the event has already happened or not), so for calculating the probability that event has to occur, we have just to focus on a restricted time frame.

In other words:
$$
V_e \sim \operatorname{Exp}\left(\frac{1}{\lambda_e}\right) \space \Longrightarrow \space Y_e \sim \operatorname{Exp}\left(\frac{1}{\lambda_e}\right)
$$
---
As the consequence of the main result, the following holds:
$$
P(E_k = e \mid X_{k-1} = x) = \frac{\lambda_e}{\Lambda(x)}
$$
Where $\Lambda(x)$ is defined as the [[DES - Definition of 'Superposition'|superposition]] of events: $\left\{E_1, E_2, \, ...\,, E_n\right\}$ defined as:
$$
\Lambda(x) = \sum_{e' \in \Gamma(x)} \lambda \, e'
$$
###### Proof:
$$
\begin{align}
P(E_k = e \mid X_{k-1} = x) &=
\\
&= P\left(Y_{e, k-1} < \underbrace{\min _{e^{\prime} \in \Gamma(x) \atop e^{\prime} \neq e} Y_{e^{\prime}, k-1}}_{\atop \LARGE \text{superposition}}\right)
\end{align}
$$
Where:
- $Y_{e, k-1}$ is an exponentially distributed with rate $\lambda_e$ 
- The superposition is exponentially distributed with rate:
$$
 \sum_{\LARGE e' \in \Gamma(x) \atop \LARGE e' \neq e} \lambda \, e'
$$
So all this probability is in the form of:
$$
P(X < Y) = \frac{\lambda_X}{\lambda_X + \lambda_Y}
$$
In our case then:
$$
\begin{align}
P(E_k = e \mid X_{k-1} = x) &=
\\[5px]
&= \frac{\lambda_e}{\lambda_e + \sum \lambda \, e'}
\\[5px]
&= \frac{\lambda_e}{\Lambda(x)}
\end{align}
$$So the problem now becomes very easy to solve for the computers, its just a problem of computing sum multiplication and divisions.

---
Exploiting the formula for $P\left(E_{k}=e \mid X_{k-1}=x\right)$ derived above, we can apply the iterative approach illustrated at the beginning for the computation of $P_{E_{k}}$ and $P_{x_{k}}$.

Let $\mathcal{E}=\{1,2, \ldots, m\}$ and $\mathcal{X}=\{1,2, \ldots, n\}$,

And define the row vectors:
$$
\begin{aligned}
&\Pi_{E}(k) \triangleq\left[P\left(E_{k}=1\right) ,\space P\left(E_{k}=2\right) ,\space \ldots ,\space P\left(E_{k}=m\right)\right] \in \mathbb{R}^{1 \times m} \\
&\Pi_{X}(k) \triangleq\left[P\left(X_{k}=1\right) ,\space P\left(X_{k}=2\right) ,\space \ldots ,\space P\left(X_{k}=n\right)\right] \in \mathbb{R}^{1 \times n}
\end{aligned}
$$
Moreover, define the matrices:
$$
P_{E} \triangleq\left[\begin{array}{cccc}
\frac{\lambda_{1}}{\Lambda(1)} & \frac{\lambda_{2}}{\Lambda(1)} & \cdots & \frac{\lambda_{m}}{\Lambda(1)} \\
\frac{\lambda_{1}}{\Lambda(2)} & \frac{\lambda_{2}}{\Lambda(2)} & \cdots & \frac{\lambda_{m}}{\Lambda(2)} \\
\vdots & \vdots & \ddots & \vdots \\
\frac{\lambda_{1}}{\Lambda(n)} & \frac{\lambda_{2}}{\Lambda(n)} & \cdots & \frac{\lambda_{m}}{\Lambda(n)}
\end{array}\right] \in \mathbb{R}^{n \times m}
$$
Where $\frac{\lambda_j}{\Lambda(i)} = P\left(E_k = j \mid X_{k-1} = i\right)$.

And,
$$
P_{X} \triangleq\left[\begin{array}{cccc}
p_{1,1} & p_{1,2} & \ldots & p_{1, n} \\
p_{2,1} & p_{2,2} & \ldots & p_{2, n} \\
\vdots & \vdots & \ddots & \vdots \\
p_{n, 1} & p_{n, 2} & \ldots & p_{n, n}
\end{array}\right] \in \mathbb{R}^{n \times n}
$$

Where $p_{i, j} \triangleq \sum p(j \mid i, e) \cdot \frac{\lambda_{e}}{\Lambda(i)}$
Which is equal to: $p_{i,j} = P\left(X_k = j \mid X_{k-1} = i\right)$

Then we have:
![[Pasted image 20220123112013.png]]

$\Rightarrow$ In matrix form:
$$
\Pi_{E}(k)=\Pi_{X}(k-1) \cdot P_{E}
$$

![[Pasted image 20220123112007.png]]

$\Rightarrow$ In matrix form:
$$
\Pi_{X}(k)=\Pi_{X}(k-1) \cdot P_{X}
$$

Notice that:
$$
\begin{aligned}
\Pi_{x}(0) &=\left[P\left(X_{0}=1\right) , \space  P\left(X_{0}=2\right) , \space \ldots , \space P\left(X_{0}=n\right)\right] 
\\[5px]
&=\left[p_{x_{0}}(1) , \space p_{x_{0}}(2) , \space \ldots , \space p_{x_{0}}(n)\right] 
\\[5px]
&(\text{Which is }\underline{\text{known}})
\end{aligned}
$$

Hence:
$$
\begin{aligned}
&\Pi_{X}(1)=\Pi_{x}(0) P_{X} 
\\[5px]
&\Pi_{X}(2)=\Pi_{x}(1) P_{X} \kern 5px = \kern 5px \Pi_{X}(0) P_{X} \cdot P_{X} \kern 5px = \kern 5px \Pi_{X}(0) P_{x}^{2} 
\\[5px]
&\Pi_{X}(3)=\Pi_{x}(2) P_{X} \kern 5px = \kern 5px\Pi_{X}(0) P_{X}^{2} \cdot P_{X} \kern 5px = \kern 5px \Pi_{X}(0) P_{X}^{3} 
\\[5px]
& \ldots
\end{aligned}
$$

We easily figure out that:
$$
\begin{aligned}
&\Pi_{X}(k)=\Pi_{X}(0) \cdot P_{X}^{k} & k=1,2,3, \ldots &
\\[5px]
&\text {Moreover, from: } \kern 10px \Pi_{E}(k)=\Pi_{X}(k-1) P_{E}: 
\\[5px]
&\Pi_{E}(k)=\Pi_{X}(0) P_{X}^{k-1} \cdot P_{E} & k=1,2,3, \ldots &
\end{aligned}
$$

$\Rightarrow$ Computing $P_{E_{k}}$ and $P_{X_{k}}$ boils down to a problem of **linear** algebra:
- Only matrix computations
- Computationally very efficient

---
### Other Stuff
![[Pasted image 20220128152314.png]]

![[Pasted image 20220128152356.png]]

![[Pasted image 20220128152520.png]]
> **ERROR**: In the previous formula

In the previous formula where it says $\frac{(\lambda T)^n}{n!}$ it should be:
$$
\frac{(\lambda T)^n}{n!} \cdot e^{-\lambda T}
$$

![[Pasted image 20220128152532.png]]

![[Pasted image 20220128152547.png]]

![[Pasted image 20220128152604.png]]

![[Pasted image 20220128152640.png]]

![[Pasted image 20220128152700.png]]

![[Pasted image 20220128152717.png]]
![[Pasted image 20220128154001.png]]

---
Covered in this lecture:
- [[DES - Definition of 'Poisson Clock Structure']]
- [[DES - Definition of 'State Holding Time']]
- [[DES - Demonstration of the State Holding Time for a Poisson Clock Structure]]
- [[DES - Poisson Distribution]]
- [[DES - Definition of a 'Poisson Process']]


