### Arguments:
[[DES - Definition of 'State Holding Time']]
[[DES - Definition of 'Poisson Clock Structure']]
[[DES - Exponential Distribution]]
[[DES - Definition of a 'Poisson Process']]

---
### Objective:
Calculate the distribution of the **State Holding Time** for a *Stochastic Timed Automata with Poisson Clock Structure*

---
###### Summary:
Starting from:
$$
F_i(t) = P(V(i) \le t)
$$
Where:
- $F_i(t)$: [[DES - (CDF) Cumulative Distribution Function|cdf]] of the state holding time of state $i$
- $V_i(t)$: [[DES - Definition of 'State Holding Time'|state holding time]] of state $i$

We want to arrive at:
$$
\begin{align}
&P(V(i) \le t) =\prod_{e \in \Gamma(x)} \sum_{n = 0}^{\infty} P\left(\text { event } e \text { occurs exactly } n \text{ times over}\left(0, t\,\right]\, \atop \underline{\text{AND}} \text{ it does NOT trigger state transition} \right)
\\[5px]
&\large P(V(x) > t) = \Huge e^{-\left\{\sum_{e \in \Gamma(x)} \lambda_e \left[1 - p(x \mid x, e)\right]\right\}t}
\\[5px]
&\Rightarrow  F_i(t) \ \text{has an exponential distribution}
\end{align}
$$
Useful to know:
$$
P\left(\text {event $e$ occurs exactly $n$ times over }\left(0, t\,\right]\,\right) = \frac{(\lambda t)^n}{n!}e^{-\lambda t}

$$
---
###### Demonstration:
Recalling that:
$$
P(V(x) \leqslant t) \ \ = \ \ 1-P(V(x)>t)
$$

we start from computing $P(V(x)>t)$, for $t > 0$.

![[Pasted image 20220123151718.png]]

Considering this small system as an example:
![[Pasted image 20220123111946.png]]
$$
\begin{align}

P(V(x) > t) &= 
\\[5px]
&= P\left(\text { no state transition occurs over }\left(0, t\,\right]\,\right)
\\[5px]
&=P\left(\bigcap_{e \in \Gamma(x)}\left\{\text { nostate transition triggered by event e over }\left(0, t\,\right] \, \right\}\right)
\\[5px]
& \text{< events are independent from each other >}
\\[5px]
&=\prod_{e \in \Gamma(x)} P\left(\text { nostate transition triggered by event } e \text { over }\left(0, t\,\right]\,\right)
\\[5px]
& = \prod_{e \in \Gamma(x)} P \left(\bigcup_{n = 0}^{\infty} \left\{ \text { event } e \text { occurs exactly } n \text{ times over}\left(0, t\,\right]\, \atop \underline{\text{AND}} \text{ it does NOT trigger state transition} \right\}\right)
\\[5px]
\end{align}
$$
- In the mini-system above $(\Delta)$ the $P\left(\text { no state transition occurs over }\left(0, t\,\right]\,\right)$ is referring to the probability that from $x$ the event $e$ occurs and the state remain $x$.
- When we say does NOT trigger state transition than that means that the "riccioli" are to only events to be considered.

"Ricciolo":
![[Pasted image 20220123153222.png]]

$$
\begin{align}
& \ldots \text{continuing from before}
\\[5px]
&=\prod_{e \in \Gamma(x)} \sum_{n = 0}^{\infty} P\left(\text { event } e \text { occurs exactly } n \text{ times over}\left(0, t\,\right]\, \atop \underline{\text{AND}} \text{ it does NOT trigger state transition} \right)
\\[5px]
\end{align}
$$
![[Pasted image 20220123154042.png]]

Where $e^{(i)}$ is the $i$-th occurrence of event $e$, and $Y_{e^{(i)}}$ its **lifetime**.
So:
$$
\begin{align}
&P\left(\text {event $e$ occurs exactly $n$ times over }\left(0, t\,\right]\,\right) = 
\\[5px]
&\kern 30px = P(Y_{e,1} + Y_{e,2} + \ldots + Y_{e,n} < t, \; Y_{e,1} + Y_{e,2} + \ldots + Y_{e,n+1} > t)
\\[5px]
&\kern 30px \text{< preliminary result >}
\\[5px]
&\kern 30px = \frac{(\lambda t)^{n}}{n !} e^{-\lambda t}
\end{align}
$$
Now lets consider instead:
$$
\begin{align}
&\prod_{e \in \Gamma(x)} \sum_{n = 0}^{\infty} P\left(\text { event } e \text { occurs exactly } n \text{ times over}\left(0, t\,\right]\, \atop \underline{\text{AND}} \text{ it does NOT trigger state transition} \right) = 
\\[5px]
&\kern 30px = \prod_{e \in \Gamma(x)} \sum_{n = 0}^{\infty} \frac{(\lambda_e t)^{n}}{n !} e^{-\lambda_e t} \,\cdot p(x \mid x, e)^n
\\[5px]
&\kern 30px = \prod_{e \in \Gamma(x)} e^{-\lambda_e t} \sum_{n = 0}^{\infty} \frac{\left[(\lambda_e t)  \,\cdot p(x \mid x, e) \right]^n}{n !}
\\[5px]
&\kern 30px \text{knowing that: } \kern 15px e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!}
\\[5px]
&\kern 30px = \Large \prod_{e \in \Gamma(x)} e^{-\lambda_e t} e^{\lambda_e \, p(x \mid x, e) \,t}
\\[10px]
&\kern 30px = \Large \prod_{e \in \Gamma(x)} e^{-\lambda_e \left[1 - p(x \mid x, e)\right]t}
\\[10px]
&\kern 30px = \Huge e^{-\left\{\sum_{e \in \Gamma(x)} \lambda_e \left[1 - p(x \mid x, e)\right]\right\}t}
\\[10px]
\end{align}
$$

So now we have that:
$$
\large P(V(x) > t) = \Huge e^{-\left\{\sum_{e \in \Gamma(x)} \lambda_e \left[1 - p(x \mid x, e)\right]\right\}t}
$$
And we can calculate:
$$
P(V(x) \le t) = 1 - P(V(x) > t)
$$
So:
$$
\begin{align}
&\large P(V(x) \le t) = \Huge 1 - e^{-\left\{\sum_{e \in \Gamma(x)} \lambda_e \left[1 - p(x \mid x, e)\right]\right\}t}
\\[10px]
&\large \text{for } t \ge 0
\end{align}
$$
We have thus shown that $V(x)$ has an exponential distribution with rate:
$$
\sum_{e \in \Gamma(x)} \lambda_e \left[1 - p(x \mid x, e)\right]
$$
Knowing that:
$$
p(x \mid x, e) + p(x' \mid x , e) \kern 10px = \kern 10px 1
$$
We can say that the rate is equal to:
$$
\sum_{\Large e \in \Gamma(x) \atop \LARGE x' \neq x} \lambda_e \ p(x' \mid x, e)
$$
Knowing this we can also say that the **average state holding time** is:
$$
\operatorname{E}\left[V(i)\right] = \frac{1}{\sum \lambda_e \ p(x' \mid x, e)}
$$

---
### More Generally:
We have considered for the example only 2 states, and only two possible events, where 1 changes state and the other doesn't, so we can say:
$$
p(x \mid x, e) + p(x' \mid x , e) \kern 10px = \kern 10px 1
$$
Then
$$
\text{Then: } \kern 5px 1 - p(x \mid x, e)\kern 10px = \kern 10px p(x' \mid x , e)
$$
So:
$$
\begin{align}
&\large \sum_{e \in \Gamma(x)} \lambda_e \left[1 - p(x \mid x, e)\right] =
\\[10px]
& \kern 30px \large = \sum_{e \in \Gamma(x)} \lambda_e \cdot p(x' \mid x, e)
\end{align}
$$
Now instead of considering only a single event that keeps me from changing state consider more events (an undefined number).
So, if we want to say the general probability of remaining in the same state, we can change:
$$
p(x \mid x, e) \to \sum_{\large e \in \Gamma(x)} p(x | x, e_i)
$$
Note that $e \in \Gamma(x)$ are all the events possible
Also that if for example the event $e_4$ would change state than $p(x \mid x, e_4) = 0$.


For the opposite instead, we are using two different states $x$ and $x'$, so the general probability for changing state can be rewritten as:
$$
\begin{align}
p(x' \mid x, e) \to  \sum_{x' \neq x}\sum_{e \in \Gamma(x)} p(x' | x, e_i)
\end{align}
$$
(Old result):
$$
\sum_{\Large e \in \Gamma(x) \atop \LARGE x' \neq x} \lambda_e \ p(x' \mid x, e)
$$
(General result):
$$
\text{rate:} \ \ \sum_{x' \neq x}\sum_{e \in \Gamma(x)} p(x' | x, e_i)
$$


---
