# Discrete Event Systems
- Corso del 1° Anno di Magistrale (1° Semestre).
- Docente: **Simone Paoletti**.
- [Link to Drive with Video Lectures](https://drive.google.com/drive/u/1/folders/0ANPVS6fxysTBUk9PVA)
										<br>
---
## Perquisites:
- [[CDS - System Theory|System Theory]]
- [[Probability]]
---
## Contents and Program:
###### *Introduction*
- [[DES - Differences Between Time-Driven Dynamics and Event-Driven Dynamics|Differences Between Time-Driven Dynamics and Event-Driven Dynamics]]
- [[DES - What are Discrete Systems|What are Discrete Systems?]]
<br>
###### *Untimed models of discrete event systems*
- Types of DESs:
	- [[DES - Model of a State Automata|'State Automata']]: **Logical (or untimed) Discrete Event-Driven System (with or without outputs)**
	***Logical***: because the system doesn't have a concept of time.
	***Discrete Event-Driven***: the system evolves only when an event occurs.
	**NOTE**: Because the system doesn't have time it's neither Discrete nor Dynamical.
	- Other types of DESs are: *Timed Automata*, *Stochastic Timed Automata*, and *Stochastic Timed Automata with Poisson Clock Structure*
<br>

###### *Timed models of discrete event systems*
- [[DES - Model of a Timed Automata|'Timed Automata']]: Same as State Automata but added the concept of time, for when events happen.
Usually these system are Dynamical, though the Event are **always** discrete so they are still non-differentiable.
<br>

###### *Stochastic timed models of discrete event systems*
- [[DES - Model of a Stochastic Timed Automata|'Stochastic Timed Automata']]: Adding also stochastic probabilities to timed automata; an event can happen at time $t$ with probability $p\in{}[0,\,1]$
- [[DES - Model of a Stochastic Timed Automata with Poisson Clock Structure|'Stochastic Timed Automata with Poisson Clock Structure']]: Particular case of Stochastic Timed Automata, where all probability distributions are exponential.
<br>

###### *Markov chains*
- 
<br>

###### *Queuing theory*
Queuing theory is the subject dedicated to the specific study of queuing systems/networks.
- 
<br>

###### *Markovian queuing networks*
Benefits of having a Continuous Time Homogeneous Markov Chain representation of the model.
- 

---
# Index - All Notes:
## Lecture Notes:
- [[DES - Lecture 7]]
- [[DES - Lecture 9]]
- [[DES - Lecture 10]]
- [[DES - Lecture 13]]
- [[DES - Lecture 14]]

## Introduction
- [[DES - Differences Between Time-Driven Dynamics and Event-Driven Dynamics]]
- [[DES - Definition of 'Dynamical']]
- [[DES - Definition of 'Discrete']]
- [[DES - What are Discrete Systems]]
	- [[DES - Definition of 'Event']]
	- [[DES - Definition of 'Static System']]
	- [[DES - Definition of 'Dynamical System']]
	- [[DES - Definition of an 'Time-Driven System']]
	- [[DES - Definition of an 'Event-Driven System']]
	- [[DES - Definition of 'Discrete-Event Dynamical System']]

## Untimed models of discrete event systems
- [[DES - Model of a State Automata]]
<br>
- [[DES - Definition of 'State of a System']]
- [[DES - Definition of 'Transition Function']]
- [[DES - Definition of 'Domain of a Transition Function']]
- [[DES - Definition of 'Feasible Event Sequence']]
- [[DES - Definition of 'State Automata']]
- [[DES - Definition of 'State Automata with Output']]

## Timed models of discrete event systems
- [[DES - Model of a Timed Automata]]
<br>
- [[DES - Definition of 'Timed Automata']]
- [[DES ~ Example of a FIFO Clock Structure]]
- [[DES ~ Example of a RR Clock Structure]]
- [[DES - Definition of an 'Time-Driven System']]
- [[DES - Definition of 'Score']]

## Stochastic timed models of discrete event systems
- [[DES - Model of a Stochastic Timed Automata]]
<br>
- [[DES - Definition of 'Expected Value']]
- [[DES - Definition of 'Variance']]
- [[DES - Uniform Distribution]]
- [[DES - Exponential Distribution]]
- [[DES - Poisson Distribution]]
- [[DES - Theorem 'Total Probability Rule']]
- [[DES - Definition of 'Stochastic Timed Automata']]

## Timed automata with Poisson clock structures
- [[DES - Model of a Stochastic Timed Automata with Poisson Clock Structure]]
<br>
- [[DES - Definition of 'Memory-Less Property']]
	- [[DES - Demonstration on the Memory-Less Property of the Exponential Distribution]]
- [[DES - Definition of 'Extended Memory-Less Property']]
	- [[DES - Demonstration of the Extended Memory-Less Property]]
- [[DES - Definition of 'Poisson Clock Structure']]
- [[DES - Definition of 'Superposition']]
	- [[DES - Demonstration of the Exponential Distribution of the Superposition]]
	- [[DES - Demonstration on How to Use the Superposition]]
- [[DES - Definition of 'State Holding Time']]
- [[DES - Theorem 'Distribution of the State Holding Time for a Poisson Clock Structure']]
- [[DES - Definition of a 'Poisson Process']]
	- [[DES - Demonstration of Poisson Process for the Probability of 0 Events Occurring in interval T]]
- [[DES - Definition of 'Stochastic Timed Automata with Poisson Clock Structure']]
	- [[DES - Demonstration of the State Holding Time for a Poisson Clock Structure]]

## Markov chains
![[Pasted image 20220127113702.png]]
- [[DES - Model of a CTHMC]]
<br>
- [[DES - Definition of 'Stochastic Process']]
	- [[DES - Definition of 'Chain']]
- [[DES - Definition of 'Independent Stochastic Process']]
- [[DES - Definition of 'Homogeneity']]
- [[DES - Definition of 'Markov Process']]
- [[DES - Definition of 'Continuous Time Homogeneous Markov Chain (CTHMC)']]
<br>
- [[DES - Definition of 'Transition Function Matrix for CTHMC']]
	- [[DES - Demonstration of the First Property of the Transition Function Matrix]]
	- [[DES - Demonstration of the Second Property of the Transition Function Matrix]]
<br>
- [[DES - Classification of the States of a CTHMC]]
- [[DES - Definition of 'Reachable State']]
- [[DES - Definition of 'Closed Subset']]
- [[DES - Definition of 'Irreducible Subset']]
- [[DES - Definition of 'Irreducible CTHMC']]
- [[DES - Definition of 'Recurrent State or Transient State']]
							<br>
- [[DES - Chapman-Kolmogorov Equation]]
	- [[DES - Demonstration of the Chapman-Kolmogorov Equation]]
- [[DES - Definition of 'Transition Rate Matrix Q']]
	- [[DES - Demonstration of the First Property of the Transition Rate Matrix Q]]
	- [[DES - Demonstration of the Second Property of the Transition Rate Matrix Q]]
	- [[DES - Demonstration of the Third Property of the Transition Rate Matrix Q]]
	- [[DES - Demonstration on How to Calculate the Transition Rate Matrix Q]]
							<br>
- [[DES - Graphical Representation of CTHMC]]
- [[DES - Graphical Transition from Stochastic State Automata with Poisson Clock Structure to CTHMC]]
							<br>
- [[DES - Transient Analysis]]
- [[DES - Steady-State Analysis]]
- [[DES - Definition of 'Limit State Probability Vector']]
- [[DES - Theorem of 'Existence, Uniqueness and Consistency of the Limit State Probability Vector']]

## Queuing Theory:
- [[DES - Definition of 'Queuing System']]
- [[DES - Definition of 'Queuing Network']]
	- [[DES - Example of Queuing Systems]]
- [[DES - Specification of Queuing Systems]]
- [[DES - Kendal's Notation]]
- [[DES - Analysis of Queuing Networks]]
- [[DES - Steady-State Conditions for Queuing Systems]]
- [[DES - Characterization of Steady-State]]
- [[DES - Little's Law]]
- [[DES - Pasta Property]]
- [[DES - Performance Indicators]]

---
## Markovian Queuing Networks:
- [[DES - Definition of 'Ergodicity']]
- [[DES - Theorem 'Ergodic CTHMC']]

---
## Discrete Systems
- [[DES - Law of Large Numbers]]
- [[DES - Central Limit Theorem]]
- [[DES - Empirical CDF]]
- [[DES - Histograms and Empirical PDF]]
- [[DES - Estimation of Models of Discrete Event Systems]]
- [[DES - Analysis of Discrete Event Systems]]
- [[DES - Definition of 'Stochastic Equivalence of Discrete-Event Models']]
- [[DES - Stochastically Equivalent CTHMC of a Discrete-Event Model]]
- [[DES - Discrete Event Simulation]]
	- [[DES - Monte Carlo Simulations]]
- [[DES - Random Number Generation]]
	- [[DES - Discrete Distributions]]
	- [[DES - Continuous Distributions]]
- [[DES - As-is and What-if Analysis]]
					<br>
- [[DES - Model of a DTHMC]]
					<br>
- [[DES - Definition of 'Discrete Time Homogeneous Markov Chain (DTHMC)']]
- [[DES - Chapman Kolmogorov Equation in Discrete Time]]
- [[DES - Transient Analysis in Discrete Time]]
- [[DES - Graphical Representation of DTHMC]]
	- [[DES ~ Example of a DTHMC]]
- [[DES - Definition of 'State-Holding Time' in Discrete Time]]
- [[DES - Geometric Distribution]]
- [[DES - Classification of States of a DTHMC]]
	- [[DES - Definition of 'Reachable State' in Discrete Time]]
	- [[DES - Definition of 'Closed Subset' in Discrete Time]]
	- [[DES - Definition of 'Absorbing State']]
	- [[DES - Definition of 'Irreducible Subset' in Discrete Time]]
	- [[DES - Definition of 'Irreducible DTHMC']]
	- [[DES - Definition of 'Recurrent State or Transient State' in Discrete Time]]
	- [[DES - Definition of 'Periodic and Aperiodic States' in Discrete Time]]
	- [[DES - Definition of 'Period of a DTHCM']]
	- [[DES - Steady States Analysis of DTHMCs]]
	- [[DES - Theorem of 'Existence, Uniqueness and Consistency of the Limit State Probability Vector' in Discrete Time]]
	- [[DES ~ Example 'How to Calculate the Limit Probability Vector of a DTHMC']]

---
### Exercises:
[[DES - All Exercises|Discrete Event Systems - All Exercises]]

-   ###### All types of exercises:
    - [ ] [[DES - Exercises with 'StateAutomata'|State Automata]]



---

## MATLAB Scripts:

----
###### All My Notes
For the best experience in reading these and all other notes, and also if you wish to EDIT them, do as follows: 
1. Install [Obsidian](https://obsidian.md), or another markdown editor.
2. Go to the Github link of this or another note
3. Download all the repo or if you know git just the 'content/' folder
4. Extract just the 'content/' folder from the repo zip file
5. Open Obsidian >> Menage Vaults >> Open Folder as Vault >> and select the 'content/' folder you just extracted

==PLEASE NOTE==:
- These notes were not revised by the professors, so take all of them with a grain of salt.
- However if you download them since they are made in markdown you can EDIT them, please do so.
- If you edit and "upgrade" them, please pass the new ones to the other students and professors.

Here are all the links to my notes:
- ***Github***: [UNISI-Sensors-and-Microsystems-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Sensors-and-Microsystems-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Sensors-and-Microsystems-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Sensors-and-Microsystems-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Complex-Dynamic-Systems-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Complex-Dynamic-Systems-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Complex-Dynamic-Systems-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Complex-Dynamic-Systems-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Discrete-Event-Systems-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Discrete-Event-Systems-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Discrete-Event-Systems-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Discrete-Event-Systems-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-System-Identification-and-Data-Analysis-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-System-Identification-and-Data-Analysis-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-System-Identification-and-Data-Analysis-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-System-Identification-and-Data-Analysis-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Multivariable-NonLinear-and-Robust-Control-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Multivariable-NonLinear-and-Robust-Control-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Multivariable-NonLinear-and-Robust-Control-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Multivariable-NonLinear-and-Robust-Control-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Artificial-Intelligence-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Artificial-Intelligence-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Artificial-Intelligence-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Artificial-Intelligence-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Human-Centered-Robotics-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Human-Centered-Robotics-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Human-Centered-Robotics-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Human-Centered-Robotics-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Machine-Learning-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Machine-Learning-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Machine-Learning-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Machine-Learning-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Bioinformatics-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Bioinformatics-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Bioinformatics-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Bioinformatics-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Network-Optimization-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Network-Optimization-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Network-Optimization-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Network-Optimization-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Mathematical-Methods-for-Engineering-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Mathematical-Methods-for-Engineering-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Mathematical-Methods-for-Engineering-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Mathematical-Methods-for-Engineering-Obsidian-Quartz-Publish).
