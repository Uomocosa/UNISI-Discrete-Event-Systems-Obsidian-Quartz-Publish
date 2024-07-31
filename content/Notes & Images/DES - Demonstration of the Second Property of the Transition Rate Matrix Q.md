Knowledge needed for this demonstration:
- [[DES - Definition of 'Transition Function Matrix for CTHMC'#^395fdd|Second property]] of the Matrix $H(t):
$$
H(t) \cdot \vec{\mathbb{1}} = \vec{\mathbb{1}}
$$
where $\vec{\mathbb{1}} = [1, \ 1, \ 1, \ 1, \ \ldots]$
- From the first part of the [[DES - Demonstration on How to Calculate the Transition Rate Matrix Q|Demonstration]] on How to calculate the Matrix Q we know that:
$$
\frac{d}{dt}H(t) = H(t) \cdot Q
$$
So:
$$
\begin{align}
0 &=
\\[5px]
&= \frac{d}{dt}\vec{\mathbb{1}}
\\[5px]
&= \frac{d}{dt}\left(H(t)\cdot\vec{\mathbb{1}}\right)
\\[5px]
&= \frac{d}{dt}\left(H(t)\right) \cdot \vec{\mathbb{1}}
\\[5px]
&= Q \cdot H(t) \cdot \vec{\mathbb{1}}
\\[5px]
&= Q \cdot \vec{\mathbb{1}}
\\[5px]
\end{align}
$$
So we have that:
$$
Q \cdot \vec{\mathbb{1}} = 0
$$
