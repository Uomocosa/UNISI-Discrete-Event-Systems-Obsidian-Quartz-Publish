### Arguments
- [[DES - Definition of 'Transition Function Matrix for CTHMC']]

---
Given the Matrix [[DES - Definition of 'Transition Function Matrix for CTHMC'#^2d24e9|H(t)]] where $p_{i,j}(t)$ is defined as:
$$
p_{i,j}(t) \triangleq P(X(s+t) = j \mid X(s) = i)
$$
Then the sum along the $i$-th row of $H(t)$ is:
$$
\sum_{\atop \Large j \in \mathcal{X}} p_{i,j}(t) = 
\sum_{\atop \Large j \in \mathcal{X}} P(X(s+t) = j \mid X(s) = i)
$$
Where we can define:
$$
\begin{align}
1 &=
\\[5px]
&= P(X(s+t) \in \mathcal{X} \mid X(s) = i) 
\\[19px]
& \text{< knowing that: } \kern 15px
	\mathcal{X} = \bigcup_{\atop \Large k} \{k\}
\kern 15px \text{>}
\\[5px]
&= P\left(\bigcup_{\atop \Large k} \left\{
	X(s+t) = j
\right\}
\mid X(s) = i
\right)
\\[5px]
&= \sum_{\atop \Large j \in \mathcal{X}} P(X(s+t) = j \mid X(s) = i)
\end{align}
$$
> The probability that at time $s+t$ (in the future) the state is one of those defined in $\mathcal{X}$ is $1$.
> It remains $1$ even if starting from one specific state $X(s) = i$
> 
> Now, $X(s+t) \in \mathcal{X}$ is defined as the union of all possible states, in this case denoted $X(s+t) = j$
> 
> Also this is always equal to say the sum over all possible state, because this is a **probability distribution**.
