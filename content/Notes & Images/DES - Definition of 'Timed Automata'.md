### Timed Automata:
A **timed automaton** is a 6-tuple ($\mathcal{E}$, $\mathcal{X}$, $\Gamma{}$, $f$, $x_0$, $V$), where:
- ($\mathcal{E}$, $\mathcal{X}$, $\Gamma{}$, $f$, $x_0$) is a [[DES - Definition of 'State Automata'|state automaton]]
- $V = \{V_e:e\in{}\mathcal{E}\}$ is a **clock structure**
	- $V_e = \{V_{e,1}\,,\;V_{e,2}\,,\;V_{e,3}\,,\;...\}$ is a **clock sequence**.
	- With $V_{e,i} > 0$  the $i$-th **lifetime** of event $e$

---

###### ~Example of a Sample Path: 
![[Pasted image 20220117192024.png]]

---

###### ~Example of Clock Structures:
[[DES ~ Example of a FIFO Clock Structure]]
[[DES ~ Example of a RR Clock Structure]]