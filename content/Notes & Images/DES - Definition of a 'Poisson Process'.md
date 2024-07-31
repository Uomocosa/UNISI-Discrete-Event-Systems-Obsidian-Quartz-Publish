###### Summary
Given a set of **independent**, events all described by the same **exponential** distribution, we have that the probability of **exactly** $n$ events occurring during the interval $[t, \ t +T]$ is:
$$
P\left(N_e(t, t+T)=n\right)=\frac{(\lambda T)^{n}}{n !} e^{-\lambda T}, \kern 30px n=0,1,2, \ldots
$$
Where $P\left(N_e(t, t+T)=n\right)$ can be seen as the [[DES - Poisson Distribution|probability mass function of the Poisson distribution]] with parameter $\lambda T$. **(From here the formula)**.

While the **average** number of said events occurring in an interval $[t, \ t + T]$ is:
$$
E\left[N_{e}(t, t+T)\right]=\lambda T \text {. }
$$
> **NOTE**:
> Both formulas do **NOT** depend on time.

---
### Poisson Process:
A Poisson process is the **counting** process of an event which is **always possible**, and characterized by interval times (interval between one event and the next) that are:
- Independent
- Identically distributed with an [[DES - Exponential Distribution|exponential distribution]].

---
### Observations:
The rate of the exponential distribution is also called the **rate of the Poisson process**.

A Poisson process can be viewed as a stochastic timed automaton with Poisson clock structure: $\left(\mathcal{E}, \mathcal{X}, \Gamma, f, x_{0}, F\right)$
- Where $\mathcal{E} = \{e\},$
- $\mathcal{X}=\{0,1,2,3, \ldots\}$, the state counts the number of occurrences of event $e$
- The transition diagram is given by: ![[Pasted image 20220123111928.png]]
- and $F=\left\{F_{e}\right\}$ with $F_{e}(t)=1-e^{-\lambda t}, \kern 10px t \geqslant 0, \, \lambda>0$. 

> **NOTE**:
> The transition diagram and the state $\mathcal{X}$ are infinite.

---
#### Observation:
Lets declare now a random variable $N_{e}(t, t+T)$ as:

$N_{e}(t, t+T) \triangleq$ number of occurrences of event $e$ over the interval $(t, t+T]$

![[Pasted image 20220123163334.png]]

$N_e(t, t+T)$ is a discrete random variable taking values in $\{0,1,2, \ldots\}$.
It can be shown that the pmf of $N e(t, t+T)$ has the following form:
$$
P\left(N_e(t, t+T)=n\right)=\frac{(\lambda T)^{n}}{n !} e^{-\lambda T}, \kern 30px n=0,1,2, \ldots
$$
Which is also the pmf of [[DES - Poisson Distribution|Poisson Distribution]] with parameter $\lambda T$
> $P[N_e(t, t+T)=n]$ : Probability that exactly $n$ events $e$ occurs in the interval $[t ,\; t + T]$

- [[DES - Demonstration of Poisson Process for the Probability of 0 Events Occurring in interval T|Demonstration]] for $n=0$ so: $P\left(N_e(t, t+T)=0\right)$

---
### Expected Value of Poisson Process
The expected value of $N_{e}(t, t+T)$ is:
$$
E\left[N_{e}(t, t+T)\right]=\lambda T \text {. }
$$
Notice that the above formula **does not depend on the time** instant $t$, but only on the length T of the interval.
$\Rightarrow$ It is a consequence of the [[DES - Definition of 'Memory-Less Property'|memory-less property]] of the exponential distribution

---
###### ~Example:
![[Pasted image 20220128152547.png]]
![[Pasted image 20220128152604.png]]
![[Pasted image 20220128152700.png]]

---