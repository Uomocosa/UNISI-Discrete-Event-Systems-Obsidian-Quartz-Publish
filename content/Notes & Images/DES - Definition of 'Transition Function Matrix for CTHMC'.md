### Transition function Matrix:
Given a [[DES - Definition of 'Continuous Time Homogeneous Markov Chain (CTHMC)'|Continuous Time Homogeneous Markov Chain]], the transition function is defined as follows:
$$
p_{i,j}(t) \triangleq P(X(s+t) = j \mid X(s) = i)
$$

^bc4308

- Independent of $s$ (for the [[DES - Definition of 'Homogeneity'|homogeneity]]).

These transition functions are arranged in the matrix:
$$
H(t) \triangleq \left[p_{i,j}(t) \right]_{i,j \in \mathcal{X}} = 
\left[
\begin{array}{cccc}
	p_{1,1}(t) & p_{1,2}(t) & p_{1,3}(t) & \ldots \\
	p_{2,1}(t) & p_{2,2}(t) & p_{2,3}(t) & \ldots & \\
	p_{2,1}(t) & p_{2,2}(t) & p_{3,3}(t)  & \ldots & \\
	\vdots & \vdots & \vdots & \ddots & \\
\end{array}
\right]
$$

^2d24e9

###### Properties of the Matrix $H(t)$:
- $H(0) = I \ , \kern 10px$ where $I$ is the **Identity Matrix**. \[[[DES - Demonstration of the First Property of the Transition Function Matrix|Dim]]\] ^d5c18f
- The sum along any row of $H(t)$ is $1$. \[[[DES - Demonstration of the Second Property of the Transition Function Matrix|Dim]]\] ^395fdd
---
###### ~Example: