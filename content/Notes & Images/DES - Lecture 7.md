### Stochastic Timed Automaton:
A [[DES - Definition of 'Stochastic Timed Automata'|stochastic timed automaton]] $\left(\varepsilon, x, \Gamma, p, p_{x_{0}}, F\right)$ transforms the stochastic clock structure $F$ into the pdf's of the event and state sequences:

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
Which translate to: "Probability that given the ($X_{k-1}$) event $x$ : the next event ($E_k$) will be $e$

---
- So the transition function $f$ will be replace with the "Transition Probability" function:
$$
P\left(x' \mid x,\,e) = P(X_{k+1} = x' \mid X_k = x, \, E_{k+1} = e\right)
$$
Where $P(x' \mid x,\,e)$ is a **conditional probability**: what is the probability that the next event will be $x'$ given the current state $x$ and the next event $e$.

---
- And the initial state $x_0$ will be replaced with a discrete random variable, described by its **probability mass function** (pmf):
$$
p_{x_0}(x_0) \triangleq{} P(X_0 = x)
$$
Where $p_{x_0}(x_0)$ is the probability that the initial state (represented by the random variable $x_0$) is $x$

---
- The lifetimes of events will be replaced with continuous random variables, described by their **cumulative distribution functions** (cdf):
$$
F_e(t) \triangleq P(V_{e,\,1} \le t)
$$
For a fixed $t \ge 0$, $F_e(t)$ is the probability that the $i$-th lifetime of event e (represented by the random variable $V_{e,\,i}$) takes values less than, or equal to $t$.

---
So now that both the state transitions and lifetime of events are governed by random variables, both the event and the state sequence must be described **probabilistically**.

These will all be random variables:
- $E_k$ : $k$-th event
- $X_0\,$: initial state
- $X_k\,$: state after the $k$-th event
- $V_{e,\,i}\,$: $i$-th lifetime of event $e$

So, $E_k$ takes values in $\mathcal{E}$ (a discrete set), then it is a discrete random variable, described by its pmf (**probability mass function**):
$$
p_{E_k}(e) \triangleq P(E_k = e) \kern 1.5pc  \forall \, e \in \mathcal{E}
$$
This will also be true for $X_k$ that takes value in the discrete set $\mathcal{X}$.

While for $V_{e,\,i}\,$, it takes place in $\mathbb{R}^{\ge 0}$ a continuous set so, it's a continuous random variable, described by its cdf:
$$
F_e(t) \triangleq P(V_{e,\,i}\, \le t) \kern 1.5pc \forall \, t \in \mathbb{R}
$$

---
### Multivariate random variable
Given two random variables: $X$ and $Y$ , if they are independent they are described by their **joint** cdf:
$$
P(X \le x, Y \le, y) = P(X \le x) \cdot P(Y \le y)
$$
Where $P(X \le x)$ e $P(Y \le y)$ are defined as **marginal probabilities**

---
### Assumptions
To simplify the description of the stochastic clock structure we make 2 assumptions:
1. Lifetimes of the same event are **identically distributed**.
2. Lifetimes of the same event, and of different events, are **independent**.

### Consequences
As a consequence of these assumptions:
$i\,$)  We have to specify **only one** cdf for each event.
$ii\,$)  **Joint cdf**'s can be obtain as the product of of marginal cdf's.

---
### Types of distributions to describe the lifetimes of the events:
- Must be a distribution defined between $[0, + \infty)$ as lifetime assume **nonnegative** numbers.
	- So for example the Gaussian (normal) distribution is not suitable for this application.

- The distribution which are suitable are:
	- The [[DES - Uniform Distribution|uniform distribution]] $\sim  U(a,b)$ 
	- The [[DES - Exponential Distribution|exponential distribution]]. $\sim  Exp(\frac{1}{\lambda})$ 
		- The exponential distribution also has the [[DES - Definition of 'Memory-Less Property'|memory-less property]]

---
### Benefits of considering variables as Independent:
Indeed, if these probabilities are known, and **independent** , then, using the [[DES - Theorem 'Total Probability Rule'|total probability rule]]:
- $P\left(E_{k}=e\right)=\sum_{x \in X} P\left(E_{k}=e \mid X_{k-1}=x\right) P\left(X_{k-1}=x\right)$
- $P\left(X_{k}=x^{\prime}\right)=\sum_{x \in X} P\left(X_{k}=x^{\prime} \mid X_{k-1}=x\right) P\left(X_{k-1}=x\right)$
$P\left(X_{k}=x^{\prime} \mid X_{k-1}=x\right)=\sum_{e \in \Gamma(x) } \underbrace{P\left(X_{k}=x^{\prime} \mid X_{k-1}=x, E_{k}=e\right)} P\left(E_{k}=e \mid X_{k-1}=x\right)$
$$
\kern 7pc p\left(x^{\prime} \mid x, e\right)
$$
$\Rightarrow$ Given $P_{x_{0}}$, we compute $P_{E_{1}}$ and $P_{x_{1}}$.
Then, given $P_{x_{1}}$, we compute $P_{E_{2}}$ and $P_{x_{2}}$.
And so on... $\Rightarrow$ iterative approach Formally,
$$
P\left(E_{k}=e \mid X_{k-1}=x\right)=P\left(Y_{e, k-1}<\min _{e^{\prime} \in \Gamma(x) \atop e^{\prime} \neq e} Y_{e^{\prime}, k-1}\right)
$$

Unfortunately, the distributions of the residual lifetimes are unknown in general, if we only assume the knowledge of the current state. Hence, $P(E_{k}=e \mid X_{k-1}=x)$ cannot be computed easily.

For this reason, to circumvent the problem, in the exercises we had to consider all the possible cases, starting from initialization, which results into a dramatic proliferation of cases as the event index $k$ increases.

---
##### ~Example:
![[Pasted image 20220122112722.png]]

- Suppose both $Y_{a, 0}$ and $Y_{b, 0}$ are **Independent Variables**.

Then to calculate $P(E_1 = a)$ we can calculate:
$$
\begin{align}
P(E_1 = a \mid X_0 = 1) & = P(Y_{a, 0} < Y_{b, 0} \mid X_0 = 1)
\\
P(E_1 = a \mid X_0 = 2) & = 0
\end{align}
$$
then, using the [[DES - Theorem 'Total Probability Rule'|total probability rule]]:
$$
\begin{align}
P(E_1 = a) & = P(Y_{a, 0} < Y_{b, 0} \mid X_0 = 1) \cdot P(X_0 = 1) + 0
\end{align}
$$
That can be easily computed in [[MATLAB - Evaluate Non-Conditional Probability|MATLAB]].


##### ~Example:
Suppose we want to find the probability $P(E_2 = a)$, then we can calculate the probability of all different cases that ends with $E_2 = a$:

![[Pasted image 20220122120148.png]]

Now looking at the clock structure we can compute these 4 probabilities:
Let's look at how to resolve the first one:

First Case Clock Strucutre:
![[Pasted image 20220122120622.png]]

Now, we do not want to calculate a triple integral, so we use [[MATLAB - Evaluate Non-Conditional Probability|MATLAB]].

Second Case Clock Structure:
![[Pasted image 20220122120918.png]]

Third Case Clock Structure:
![[Pasted image 20220122121036.png]]

Fourth Case Clock Structure:
![[Pasted image 20220122121159.png]]

> **NOTE**: 
> Looking at the Second and Fourth Clock Structures we can see that the probability of $P(V_{a, 1} < V_{b, 1}) = P(V_{a, 2} < V_{b, 1})$, if $a$ supports the [[DES - Definition of 'Memory-Less Property'|memory-less property]] and $a$ and $b$ are **independent**.


---
### Introduction to Poisson Clock Structures
The computational complexity of calculating these probability increases the more event we take into account in the system.

The question now is whether there exist classes of stochastic timed automata for which computing $P\left(E_{k}=e \mid X_{k-1}=x\right)$ is an easy task.

- The answer is given by stochastic timed automata with [[DES - Definition of 'Poisson Clock Structure'|Poisson clock structure]].
- Or even **simulate the problem** using for example the [[DES - Monte Carlo Simulations|Monte Carlo methods]]

---

###### ~Example: 
![[10 - Poisson clock structure(3-4)_211218_153036.pdf]]