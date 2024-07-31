As we know from the [[DES - Definition of 'Transition Rate Matrix Q'|Definition of 'Transition Rate Matrix Q']]
- The entries of $p_{i,j}$ are **nonnegative** for $j \neq i$
- And the sum of The sum along any row of $Q$ is $0$

As we stated in the demonstrations these properties are verified, but to be both true we have that the remaining entries ($p_{i,i}$) must be **nonnegative**

Also each entry $p_{i,i}$ have to be the sum of the $p_{i,j}$ for $i \neq j$ of the same row changed of sign, so:
$$
p_{i,i} = - \sum_{i} p_{i,j}
$$