### Score:
The **score** of event $e$ at time $t$ , denoted $n_e(t)$, is the number of total **[[DES - Definition of 'Timed Automata'|lifetimes]]** of event $e$ used up to time $t$.
- At time $t$, the score $n_e(t)$ is the index to the current position in the clock sequence of event $e$
![[Pasted image 20220117193443.png]]
- It means that $V_{e,1}$ and $V_{e,2}$ have been used, whereas $V_{e,3}$ has not been used yet.

---
###### ~Example:
![[Pasted image 20220117193504.png]]