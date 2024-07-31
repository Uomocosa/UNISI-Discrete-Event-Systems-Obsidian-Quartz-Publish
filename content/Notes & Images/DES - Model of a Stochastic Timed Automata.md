###### Summary
The more general case of *Timed Automata*, where we change from deterministic time and event to stochastic (random) ones.

We define the probability of being in each state at the beginning ($p_{x_0}$)
- Es.: $p_{x_0} = \left[ \frac{1}{3}, \ \frac{2}{3} \right]$

We define the probability transition function ($p$)
- Es.: $p(1 \mid 2, \ b) = 1 -q$  : probability of going from state $2$ to state $1$ after event $b$ has occurred is equal to $1-q$.

We define the distribution function of the events ($F$)
- $F_a \sim \operatorname{U}(0,4) \ s$ :  **Uniform** distribution ($\text{U}$) 

> **NOTE**:
> Not all changes have to be made, the system can be better described by a **Mixed Stochastic Timed Automata**, where some part of the system are still deterministic, while other are considered as stochastic

----
# Stochastic Timed Automata
Stochastic means that we will have to use random variables, define by specific [[DES - (PDF) Probability Distribution Function|probability distribution functions (pdf)]], [[DES - (CDF) Cumulative Distribution Function| cumulative distribution functions (cdf)]] and [[DES - (PMF) Probability Mass Function|probability mass functions]].

As we will see this stochastic variables can be integrated with the [[DES - Model of a Timed Automata|Timed Automata]], specifically we can change the clock structure to describe the randomness that the events can have (we denote a stochastic clock structure with $F$, while a deterministic one as we have seen previously with $V$), this also applies to initial state, and the transition function.

 || Deterministic | Stochastic
------------- | ------------- | -------------
**Clock Structure** | $V$ | $F$
**Transition Function** | $f$ | $p$
**Initial Condition** | $x_0$ | $p_{x_0}$

To understand what $\left( p, \ p_{x_0}, \ F \right)$ means let's look at an example:
$$
\begin{align}
&p_{x_0} = \left[ \frac{1}{3}, \ \frac{2}{3} \right]
\\
\\
&\left.
\begin{array}[]
\ F_a \sim \operatorname{U}(0,4) \ s \
\\
\ F_b \sim \operatorname{Exp}(\frac{1}{2}) \ s \
\end{array}
\right\} \ F= [F_a, \ F_b]
\\
\\
& p(2 \mid 1, \ a) = 1 
\\
& p(1 \mid 2, \ b) = 1 - q
\\
& p(2 \mid 2, \ b) = q
\end{align}
$$
![[SmartSelect_20220128-110450_Samsung Notes.jpg]]

Where: 
- $p_{x_0} = \left[ \frac{1}{3}, \ \frac{2}{3} \right]$  : means that there is a 33% chance ($\frac{1}{3}$) of starting in state $1$ and a 66% chance of starting is state $2$.
- $F_a \sim \operatorname{U}(0,4) \ s$ : means that the event $a$ is described by a **Uniform** distribution ($\text{U}$) in the interval $[0,4]$.
- $F_b \sim \operatorname{Exp}(\frac{1}{2}) \ s$ : means that the event $b$ is described by an **Exponential** distribution ($\text{Exp}$) with **rate** $2 \ s^{-1}$ (~ex.: in this case the rate is described as 2 events over 1 second, is an exponential distribution so this is the average value).
- $p(1 \mid 2, \ b) = 1 -q$  : means that the probability of going from state $2$ to state $1$ after event $b$ has occurred is equal to $1-q$.

---
### Definition of 'Stochastic Timed Automata'
This brings us to how we can define the stochastic time automata:
 - [[DES - Definition of 'Stochastic Timed Automata']]
Notice the differences with the [[DES - Definition of 'Timed Automata']], like how they were described before:
- $x_0$ -> $p_{x_0}$
- $f$ -> $p$
- $V$ -> $F$

---
### Mixed Timed Automata
Any combination of Stochastic Timed Automata $\left(\mathcal{E}, \ \mathcal{X}, \ \Gamma, \ p, \ p_{x_{0}}, \ F\right)$ and Timed Automata $\left(\mathcal{E}, \ \mathcal{X}, \ \Gamma, \ f, \ x_0, \ V\right)$
- $\left(\mathcal{E}, \ \mathcal{X}, \ \Gamma, \ f, \ p_{x_{0}}, \ F\right)$
- $\left(\mathcal{E}, \ \mathcal{X}, \ \Gamma, \ f, \ x_0, \ F\right)$
- $\left(\mathcal{E}, \ \mathcal{X}, \ \Gamma, \ f, \ p_{x_{0}}, \ V\right)$
- $\left(\mathcal{E}, \ \mathcal{X}, \ \Gamma, \ p, \ x_0, \ F\right)$
- $\left(\mathcal{E}, \ \mathcal{X}, \ \Gamma, \ p, \ x_0, \ V\right)$
- $\left(\mathcal{E}, \ \mathcal{X}, \ \Gamma, \ p, \ p_{x_{0}}, \ F\right)$
$\ldots$

---
### Total Probability Rule:
Very important theorem that will be useful in the future demonstrations.
- [[DES - Theorem 'Total Probability Rule']]

The important formulas are:
$$
P(A)=\sum_{i=1}^{n} P\left(A \mid B_{i}\right) \cdot{} P\left(B_{i}\right)
$$
And:
$$
P(A \mid C)=\sum_{i=1}^{n} P\left(A \mid B_{i}\,,C\right) \cdot{} P\left(B_{i} \mid C\right)
$$

---