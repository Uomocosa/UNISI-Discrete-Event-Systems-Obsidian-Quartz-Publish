### Arguments
[[DES - Definition of 'Transition Function Matrix for CTHMC']]

---
Given the Matrix [[DES - Definition of 'Transition Function Matrix for CTHMC'#^2d24e9|H(t)]] where $p_{i,j}(t)$ is defined as:
$$
p_{i,j}(t) \triangleq P(X(s+t) = j \mid X(s) = i)
$$
Then:
$$
p_{i,j}(0) = P(X(s) = j \mid X(s) = i) = \left\{
\begin{array}{cc}
	1 & if \kern 10px i = j
	\\[5px]
	0 & if \kern 10px i \neq j
\end{array}
\right.
$$
> What is the probability that the state is $j$ when the state is $i$ : $0$
> What is the probability that the state is $j$ when the state is $j$ : $1$