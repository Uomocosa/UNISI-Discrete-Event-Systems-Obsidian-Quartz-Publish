### Arguments:
[[DES - Definition of 'Transition Function Matrix for CTHMC']]

---
###### Summary: Declaration of $H(t)$ and $Q$ in respect to each other
[[DES - Demonstration on How to Calculate the Transition Rate Matrix Q#Declaration of H t and Q in respect to each other|Complete Demonstration]]
Starting from:
$$
H(t + a) = H(t)\cdot H(a) 
$$
We want to arrive at:
$$
H(t) = e^{Qt}
$$
(Obtained from a solution to a Cauchy Problem)
Where:
$$
Q \triangleq \lim_{dt \to 0} \frac{H(dt) - I}{dt}
$$
---
###### Summary: Check that the limit is actually equal to $Q$
[[DES - Demonstration on How to Calculate the Transition Rate Matrix Q#Check that the limit is actually equal to Q|Complete Demonstration]]
Starting from:
$$
\begin{align}
&\lim_{dt \to 0} \frac{H(dt) - I}{dt}
\\[5px]
&H(0) = I
\\[5px]
&H(t) = e^{Qt}
\end{align}
$$
We want to arrive at:
$$
\lim_{dt \to 0} \frac{H(dt) - I}{dt} = Q
$$
---
###### Summary: Brake the Recursion of $H(t)$ and $Q$
[[DES - Demonstration on How to Calculate the Transition Rate Matrix Q#Brake the Recursion of H t and Q|Complete Demonstration]]
Starting from:
$$
\begin{align}
&Q = \left[
\begin{array}{ccc}
	q_{1,1} & q_{1,2} & \dots
	\\
	q_{2,1} & q_{2,2} & \dots
	\\
	\vdots & \vdots & \ddots
\end{array}
\right]
\\[5px]
&q_{i,i} = -\sum_{j \neq i} q_{i,j}
\\[5px]
&H(dt) = I + Q \cdot dt + o(dt)
\\[5px]
&H(t) = e^{Qt}
\end{align}
$$
We want to arrive at:
$$
F_i(t) = 1 - e^{\large-q_{i,i} t}
$$
Useful to know:
$$
\begin{align}
&F_i(t) = P(V(i) \le t)
\\[5px]
&P(V(i) \le t+dt \mid V(i) > t) = \sum_{j \neq i} p_{i,j}(dt)
\end{align}
$$
> Note that the matrix $H(t)$ describes the probability transitions from state $i$ to state $j$, so the probability of changing state in time $dt$ is equal to the sum of all **rows** of $p_{i,j}$ excluding $j = i$ because that is the probability of remaining in state $i$.

Where:
- $F_i(t)$ [[DES - (CDF) Cumulative Distribution Function|cdf]] of state holding time of state $i$
- $V(i)$ [[DES - Definition of 'State Holding Time'|State Holding Time]] of state $i$

---
###### Summary: Compute $H(t)$ from $Q$
[[DES - Demonstration on How to Calculate the Transition Rate Matrix Q#Compute H t from Q|Complete Demonstration]]
Starting from:
$$
\begin{align}
&p_{i,j}(t) \triangleq P(X(s+t) = j \mid X(s) = i)
\\[5px]
&p_{i,j}(dt) = q_{i,j}\cdot dt \kern 30px \text{for $i \neq j$}
\end{align}
$$
We want to arrive at:
$$
p_{i,j} = - \frac{q_{i,j}}{q_{i,i}}
$$
Useful to know:
$$
\begin{align}
p_{i,j} &= P\left(\bigcup_{t \ge 0} \left\{X(t+dt) = j \mid X(s) = i \ \ \forall \ s\in [0, \ t]\right\}\right)
\\[10px]
&= \int_{0}^{\infty} \left\{X(t+dt) = j \mid X(s) = i \ \ \forall \ s\in [0, \ t]\right\}
\end{align}
$$
> **NOTE**: in this equations $p_{i,j}$ does **NOT** depend on time, when we write $p_{i,j}$ without the dependency on time, we are talking about the probability that the next event (whenever it will happen) will change the state from $i$ to $j$

---
### Declaration of $H(t)$ and $Q$ in respect to each other
Arguments:
$$
\begin{align}
&H(t + a) = H(t)\cdot H(a)
\\[5px]
&H(0) = I
\end{align}
$$
![[408213db-147c-498d-a35b-a7d27635e5c9-01 1.png]]
![[408213db-147c-498d-a35b-a7d27635e5c9-02 1.png]]

---
### Check that the limit is actually equal to $Q$
Arguments:
$$
\begin{align}
&\lim_{dt \to 0} \frac{H(dt) - I}{dt}
\\[5px]
&H(0) = I
\\[5px]
&H(t) = e^{Qt}
\end{align}
$$

![[408213db-147c-498d-a35b-a7d27635e5c9-03 1.png]]

---
### Brake the Recursion of $H(t)$ and $Q$
Arguments:
$$
\begin{align}
&Q = \left[
\begin{array}{ccc}
	q_{1,1} & q_{1,2} & \dots
	\\
	q_{2,1} & q_{2,2} & \dots
	\\
	\vdots & \vdots & \ddots
\end{array}
\right]
\\[5px]
&q_{i,i} = -\sum_{j \neq i} q_{i,j}
\\[5px]
&H(dt) = I + Q \cdot dt + o(dt)
\\[5px]
&H(t) = e^{Qt}
\end{align}
$$

![[408213db-147c-498d-a35b-a7d27635e5c9-04 1.png]]
![[408213db-147c-498d-a35b-a7d27635e5c9-05 1.png]]
![[408213db-147c-498d-a35b-a7d27635e5c9-06 1.png]]

We know that:
$$
H(dt) = I + Q \cdot dt + o(dt)
$$
So we can say that:
$$
\begin{align}
&p_{i,j}(dt) = 0 + q_{i,j}\cdot dt \kern 30px \text{for $i \neq j$}
\\[5px]
&p_{i,j}(dt) = 1 + q_{i,j}\cdot dt \kern 30px \text{for $i = j$}
\end{align}
$$

![[408213db-147c-498d-a35b-a7d27635e5c9-07 1.png]]
![[408213db-147c-498d-a35b-a7d27635e5c9-08 1.png]]
![[408213db-147c-498d-a35b-a7d27635e5c9-09 1.png]]

---
### Compute $H(t)$ from $Q$
Arguments:
$$
p_{i,j}(t) \triangleq P(X(s+t) = j \mid X(s) = i)
$$

![[408213db-147c-498d-a35b-a7d27635e5c9-10 1.png]]
![[408213db-147c-498d-a35b-a7d27635e5c9-11 1.png]]
![[408213db-147c-498d-a35b-a7d27635e5c9-12 1.png]]
