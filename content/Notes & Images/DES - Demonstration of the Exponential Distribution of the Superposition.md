### Arguments:
[[DES - Exponential Distribution]]

---
Given the event $X_i \sim Exp\left(\frac{1}{\lambda_i}\right)$ for $i = 1, \ 2, \ 3, \ \ldots, \ n$
What is the distribution of $X$ ?
![[Pasted image 20220122173234.png]]
![[Pasted image 20220122173322.png]]

Now, remember that being an exponential distribution we have that:
$$
P(X_i > t) = \ - e^{- \lambda_i t}
$$
So:
$$
= 1 \ - \ e^{-\lambda_1 t}\cdot- e^{-\lambda_2 t}\cdot \ldots \cdot - e^{-\lambda_n t}
$$
Which can be seen as:
$$
= 1 - e^{-\left(\lambda_1 + \lambda_2 + \, ... \, + \lambda_n\right)t}
$$
So the distribution of the superposition is:
$$
P(X \le t) = 1 - e^{-\left(\lambda_1 + \lambda_2 + \, ... \, + \lambda_n\right)t}
$$
$\Rightarrow$ The **superposition** of  $X_1$, $X_2$, ..., $X_n$ has an **exponential distribution** with **rate**:
$$
\Lambda = \lambda_1 + \lambda_2 + \, ... \, + \lambda_n
$$