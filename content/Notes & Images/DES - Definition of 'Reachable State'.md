### Reachable State:
State $j \in \mathcal{X}$ is **reachable** from state $i \in \mathcal{X}$ if $p_{i,j}(t) > 0$ for some $t >0$

This condition is equivalent to the existence of an oriented path from $i$ to $j$ in the _graph representation_ of the [[DES - Definition of 'Continuous Time Homogeneous Markov Chain (CTHMC)'|CTHMC]]

---
###### ~Example:
![[Pasted image 20220125170126.png]]

State $1$ is reachable by $2$ and $3$.
State $2$ is reachable by $1$ and $3$.
State $3$ is **NOT** reachable by any other state.