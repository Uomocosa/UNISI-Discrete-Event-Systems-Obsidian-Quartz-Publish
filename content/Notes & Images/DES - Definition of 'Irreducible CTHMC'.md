### Irreducible CTHMC:
The CTHMC is said **irreducible** if the state set $\mathcal{X}$ is [[DES - Definition of 'Irreducible Subset'|irreducible]]

---
###### ~Example: Irreducible CTHMC
![[Pasted image 20220125170714.png]]

State $1$ is reachable from states $2$, $3$
State $2$ is reachable from states $1$
State $3$ is reachable from states $2$
State $4$ is reachable from states $2$
State $5$ is reachable from states $3$, $4$, $6$
State $6$ is reachable from states $4$, $5$
Every state is reachable by at least one different state set, so this state set is **Irreducible** and so it is the CTHMC.
