### Arguments:
- $X \sim Exp\left(\frac{1}{\lambda}\right)$
- $f_Y(y) = 0 \kern 10px \text{for} \kern 10px y \le 0$, 
	- where: $f_Y$ denotes the [[DES - (PDF) Probability Distribution Function|pdf]] of $Y$.
- Moreover, let $s \ge 0$.

![[Pasted image 20220122171103.png]]
![[Pasted image 20220122171246.png]]

Also for the hypothesis we have that $Y$  is always positive and so is $X$ (from the definition of the [[DES - Exponential Distribution#PDF|pdf of the exponential distribution]]).
So we are interested only on the first quadrant, where it applies that $x > y + s$

![[Pasted image 20220122171306.png]]
![[Pasted image 20220122171534.png]]

We can integrate $x$ from $y+s$ instead of $0$ because $x = 0$ for $x \le y+s$ as we can see from the graph before.

![[Pasted image 20220122171628.png]]
![[Pasted image 20220122171711.png]]
![[Pasted image 20220122172022.png]]
![[Pasted image 20220122172101.png]]

---