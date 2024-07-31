###### Summary
If we know the **lifetime** of the events in a system, and they are **deterministic** (~ex.: event $e_{a_1}$ will happen @ 2:30, $e_{b_1}$ @ 2:45, $e_{a_2}$ @ 3:00, $e_{a_3}$ @ 4:20, ...), then we can use a Timed Automata to describe the system.


> A Timed Automata can be defined using 6-tuple ($\mathcal{E}, \ \mathcal{X}, \ \Gamma, \ f,  \ x_0, \ V$):
> - ($\mathcal{E}, \ \mathcal{X}, \ \Gamma, \ f,  \ x_0$) : the same as state automata.
> - $V$ :  **Clock Structure** (~ following the ex. before: {$V_{a_1} = 150 \ s$, $V_{b_2} = 15 \ s$, $V_{a_2} = 15 \ s$, $V_{a_3} = 120 \ s$, ...})
> 	- where: $V_{e_i}$: **lifetime** of event $e_i$

We define an event dependent on time as: **Event** $\triangleq$ the outcome of a process.

Event terminology:
- an event is **activated**, when the corresponding process is started.
- an event is **paused**, when the corresponding process is stopped temporarily.
- an event is **resumed**, when the corresponding process is restarted after a pause.
- an event is **cancelled** (or **killed**), when the corresponding process is stopped and will not be resumed.
- an event **occurs** when the corresponding process is terminated.

**Score** of an event $\triangleq$ how many times the event occurred.


Given a State Automata described by the 5-tuple ($\mathcal{E}, \ \mathcal{X}, \ \Gamma, \ f,  \ x_0$):
Then we

---
# Timed Automata
Expand the [[DES - Model of a State Automata|State Automata]] with the concept of time.
- Given a [[DES - Definition of 'Feasible Event Sequence'|feasible event sequence]], the State Automata returns the corresponding state (or output) sequence: $\{y_0\;y_1\;y_2\;...\}$
- No information about **when** events (and therefore state transition) occur
	- Needed for example, to draw the sample path (or state trajectory) of the system:
	
![[Pasted image 20220117184456.png]]

---
We **cannot** simply add time at the sequence of events:
$\{e_1,\;e_2,\;e_3,\;...\}\to{}\{e_1(t)\;e_2(t)\;e_3(t)\;...\}$
Because for example if a processor that executes tasks has a [[FIFO]] scheduling policy, or a [[RR]] one we cannot establish a correct system without this information.

So the **time instants** when events occur are dependent variables of the DES, they are **outputs** of the timed models.

[[DES ~ Example of a FIFO Clock Structure|Example of a FIFO queue]]
[[DES ~ Example of a RR Clock Structure|Example of a RR queue]]

---
###### Notice that:
- In the previous examples, execution times of each task were independent of the system (they were properties of each task, depending on the number of instructions each task consisted of).
- Conceptually, execution times are total **durations** of the execution **process** of each tasks.
- An event d (termination of the execution of a task) **occurs** at the end of the corresponding execution process.
---
### Modelling assumptions:
- An [[DES - Definition of 'Event'|event]] is the outcome of a process.
- The process is typically unspecified, and described only by its duration.

![[Pasted image 20220117191225.png]]

So we give this definition to [[DES - Definition of 'Timed Automata'|Timed Automata]]

---
#### Terminology for events
We first introduce some terminology. We say that:
- an event is **activated**, when the corresponding process is started.
- an event is **paused**, when the corresponding process is stopped temporarily.
- an event is **resumed**, when the corresponding process is restarted after a pause.
- an event is **cancelled** (or **killed**), when the corresponding process is stopped and will not be resumed.
- an event **occurs** when the corresponding process is terminated.

---
#### Score:
[[DES - Definition of 'Score']]

---
#### Basic Example of Event Timing Dynamics

![[05 - Timed automata(9-12)_211218_153610.pdf]]

---
#### Note:
When writing an algorithm to simulate a system, we always have to tweak some part of it, **NO GENERAL ALGORITHM CAN BE USED FOR SYSTEM SIMULATION**.

---
#### TODO: Rules for transforming a clock structure (input) into a sample path (output):
The following rules define the **event timing dynamics** of a timed automaton.

---