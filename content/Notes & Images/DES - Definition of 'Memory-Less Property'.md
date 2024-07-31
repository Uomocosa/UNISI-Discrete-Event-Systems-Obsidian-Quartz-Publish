### Memory-Less Property:
The memory-less property for a [[DES - Definition of 'Probability Distribution'|probability distribution]] state that:
$$
P(X > t + s \mid X > t) \ \ = \ \ P(X > s)
$$
---
###### ~Example: where the memory-less property is NOT valid
To understand the term "memory-less" for this property, assume that $X$ models the time to failure of an electronic component.

At time (when the component is **new**) we compute the probability that the component does not fail.

In the next year (**the first year**): $P(X > s = 1 \space \text{year})$.

Then, we observe that the component does not fail in the first three years: $X > t = \text{ 3 years}$.

 With these knowledge, we compute the probability that the component does not fail in the next year (**the fourth year**): $P(X > t+s = \text{ 4 years} \mid X > t = \text{3 years})$.

 For the memory-less property, this probability equals $P(X > t = \text{1 year})$  ==computed when the component was new==
 ... but now is 3 years old.

 $\Rightarrow$ The Memory-Less Property: the component does not "remember" that it is getting older.

---
##### Other Useful links:
- [[DES - Demonstration on the Memory-Less Property of the Exponential Distribution]]
