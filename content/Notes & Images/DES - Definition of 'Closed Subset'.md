### Closed Subset:
A subset $S \subseteq \mathcal{X}$ is **closed** if $q_{i,j} = 0 \kern 15px \forall \,i \in S, \ j \notin S$ 

Equivalently, there are no arcs starting from state in $S$ and ending in states **not** in $S$.
Or, when the system enters the subset $S$, it remains in $S$ forever.

---
###### ~Example: 
![[Pasted image 20220125170714.png]]

The subset $S = \{4, \ 5, \ 6\}$ is **closed**.
The subset $S = \{1, \ 2, \ 3\}$ is not closed.
> **NOTE**: Also the state set $\mathcal{X} = \{1, \ 2, \ 3, \ 4, \ 5, \ 6\}$ is **closed**.