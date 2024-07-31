### Poisson Clock Structure
A Poisson clock structure is a stochastic clock structure $F=\left\{F_{e}: e \in \mathcal{E}\right\}$ where all the distributions $F_e$ are [[DES - Exponential Distribution|exponential]].
i.e. for all $e \in \mathcal{E}$ :
$$
F_{e}(t)=\left\{\begin{array}{cl}
1-e^{-\lambda e t} & \text { if } t \geqslant 0 \\
0 & \text { otherwise. }
\end{array} \quad \lambda_{e}>0\right.
$$
The Poisson Clock Structure holds an important property due to the [[DES - Definition of 'Memory-Less Property'|memory-less property]] of the exponential distribution:
$$
\forall \, e \in \Gamma(x) \kern 30px 
V_e \sim \operatorname{Exp}\left(\frac{1}{\lambda_e}\right) \space \Longrightarrow \space Y_e \sim \operatorname{Exp}\left(\frac{1}{\lambda_e}\right)
$$
Where:
- $V_e$ is the total lifetime of event $e$
- $Y_e$ is the remaining lifetime of event $e$

---
##### Demonstration by induction:
1. At initialization ($k = 0$):
$$
Y_{e,0} = V_{e,1} \kern 30px \text{for all} \kern 10px e \in \Gamma(x_0) 
$$
$\Rightarrow$ Since we know from the model:
$$
V_{e,1} \sim \operatorname{Exp}\left(\frac{1}{\lambda_e}\right)
\kern 10px \Longrightarrow \kern 10px
Y_{e,0} \sim \operatorname{Exp}\left(\frac{1}{\lambda_e}\right)
$$
> For $k = 0$, the distribution of the residual lifetime is equal to the distribution of the total lifetime
> $\Rightarrow$ So the statement is true for $k = 0$


2. We assume that the statement is true for $k-1$, 
$$
Y_{e,k-1} \sim \operatorname{Exp}\left(\frac{1}{\lambda_e}\right)
$$
And then we prove that it is true for $k$.
$$
Y_{e,k} \sim \operatorname{Exp}\left(\frac{1}{\lambda_e}\right)
$$

So, we divide the possible cases: 
- Case $i$. Event $e$ is activated in state $X_k$, so it started and it can occur.
$$
Y_{e,k} = V_{e,N_e,k}
$$
> $\Rightarrow$ The $k$-th residual lifetime of event $e$ is equal to the total life time from the clock sequence of event $e$.
> And since, $V_{e,N_e,k}$ is for hypothesis an exponential distribution, then $Y_{e,k}$ is also an exponential distribution with the same $\lambda$
$$
\begin{align}
\text{since}\kern 10 px V_{e,N_e,k} \sim & \space \operatorname{Exp}\left(\frac{1}{\lambda_e}\right)
\\
\text{then,}\kern 10 px Y_{e,k} \sim & \space \operatorname{Exp}\left(\frac{1}{\lambda_e}\right)
\end{align}
$$
- Case $ii$. Event $e$ "continues" in state $X_k$: event $e$ does not occur but another event happens before $e$
So there exist an event $a$ which residual lifetime is less the the residual lifetime of event $e$.
![[Pasted image 20220123133512.png]]

So the $k$-th residual lifetime of event $e$ is:
$$Y_{e,k} = Y_{e,k-1} - Y_{a,k-1}$$
So:
$$
\begin{align}
P\left(Y_{e,k} \le t \mid Y_{e,k-1} > Y_{a,k-1}\right) &= 
\\ 
&= \space P\left(Y_{e,k-1} - Y_{a,k-1} \le t \mid Y_{e,k-1} > Y_{a,k-1}\right)
\\
&= \space P\left(Y_{e,k-1} \le Y_{a,k-1} + t \mid Y_{e,k-1} > Y_{a,k-1}\right)
\\[5px]
& \text{< using the memory less property >}
\\[5px] 
&= \space P\left(Y_{e,k-1} \le t \right)
\\
\end{align}
$$
> The probability of event $e$ at state $k$ to happen is the same as the probability of event $e$  at state $k-1$
> 
> Now this is always true if we also suppose that event $e$ at state $k$ is not killed, and its $\lambda_e$ doesn't change.

