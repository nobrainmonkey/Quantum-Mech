We want to study the type of the problem where 
$$
H = H_{0} + \lambda H_{1}(t) \tag{1} 
$$
where $H_{0}$ is exactly solved (with $\epsilon_{n}$ and $\ket{n}$) and we want to study $\lambda H_{1}$ 
___
We start with TDSE
$$
i \hbar \frac{\partial}{\partial t} \ket{ \psi(t)}= (H_{0}+\lambda H_{1}(t)) \ket{\psi} \tag{2}   
$$
We will express 
$$
\begin{align}
\ket{\psi(t)}  & = \sum_{n} c_{n}(t) \ket{n}  \\
& = \sum_{n} a_{n}(t) e^{-i \epsilon_{n} t/ \hbar} \ket{n} 
\end{align} \tag{3} 
$$
where we separated the dynamic phase out.
Combine $(3)$ and $(1)$ yields:
$$
\sum_{n}\left[ i \hbar \frac{d a_{n}}{dt} + \epsilon_{n}a_{n}(t)  \right]e^{-i\epsilon_{n}t/\hbar} \ket{n}= \sum_{n}[\epsilon_{n} a_{n}(t)+ \lambda H_{1}(t)a_{n}(t)] e^{-i \epsilon_{n}t /\hbar} \ket{n} 
$$
where  we can see that $\epsilon_{n}a_{n}(t)$ terms cancel.
We then tank an inner product with $\bra{m}$ and we know $\braket{ m | n }=1$ . This get us:
$$
i \hbar \frac{d a_{m}}{dt} e^{-i \epsilon_{m}t/\hbar}=\lambda \sum_{n}\bra{m} H_{1}(t) \ket{n} e^{-i\epsilon_{n}t/\hbar} a_{n}(t)
$$
Define $\hbar \omega_{mn} \equiv (\epsilon_{m}-\epsilon_{n})$ $\implies$ 
$$
i \hbar \dot{a}_{m} = \lambda \sum_{n} \bra{m} H_{1} \ket{n} e^{i \omega_{mn}t}a_{n}(t)
$$
which is an exact result. Next, we approximate $a_{n}$ as 
$$
a_{n}(t) = a_{n}^{0} + \lambda a_{n}^{1} + \lambda^{2} a_{n}^{2}+ \dots
$$
Please check that 
$$
i\hbar \dot{a}_{m}^{r+1} = \sum_{n} \bra{m} H_{1}\ket{n} e^{i \omega_{mn}t}a_{n}^{r}(t) \tag{4} 
$$
where $a_{n}^{0}$ are known and is defined by $\psi(0) =  \sum_{n} a_{n}^{0} \ket{n}$. We will only do this for first order P.T. Therefore, $r=0$ for $\dot{a}_{n}^{1}$ .
___
Let $H_{1}(t)=0$ for $t<0$, and initial condition $\psi(0)=\ket{i} \leftrightarrow a_{n}^{0} = \delta_{n,i}$ 
simplify notation: $a^{1}_{n}(t) = a_{n}(t)$ .
Apply $(4) \implies$
$$
i \hbar \frac{d a_{f}}{dt} =\bra{f} H_{1}(t)\ket{i} e^{i \omega_{fi}t} 
$$

Solving this get 
$$
a_{f}(t) = \delta_{fi} - \frac{i}{\hbar} \int_{0}^{t} \bra{f} H_{1}(t') \ket{i} e^{i \omega_{fi}t'}  \, dt' \tag{5}  
$$
Note that when t=0, the integral term in $(5)$ is trivially zero. However, then $t>0$, we can see that some probabilities leaks from $\ket{i}$ into other states $\ket{f}$ where $\braket{  f|\psi(t)  } = a_{f}(t)e^{i \epsilon_{f}t/\hbar}$ .

Note that this approximation is valid when the integral part of $(5)$ is small in comparison to $1$ , or $\lvert a_{f}(t) \rvert \ll \forall f \neq i$.

___
Two perturbations that are very important:
1. Constant perturbation $H_{1}(t) = \Theta(t)$ 
2. sinusoidal $H_{1}(t)= 2V_{0} \cos(\omega t) \Theta(t)$ 
Let us focus on 2. as 1. is nothing but the limit of $\omega \to 0$.

For $f \neq i$ 
$$a_{f}(t) = - i\hbar \bra{f} \hat{V}_{0} \ket{i} \int_{0}^{t} e^{i (\omega_{fi}+\omega)t'} + e^{i( \omega_{fi}-\omega)t'} \, dt'$$ 
Where the integral becomes 
$$
\frac{e^{i (\omega_{fi} + \omega)t}-1}{i (\omega_{fi}+\omega)} + \frac{e^{i(\omega_{fi}- \omega)t}-1}{i(\omega_{fi}- \omega)}
$$
Therefore, 
$$
P_{i\to f} = \frac{\lvert V_{fi} \rvert ^{2}}{\hbar^{2}} \lvert
\frac{e^{i (\omega_{fi} + \omega)t}-1}{i (\omega_{fi}+\omega)} + \frac{e^{i(\omega_{fi}- \omega)t}-1}{i(\omega_{fi}- \omega)}\rvert ^{2}
$$
Note that for constant case, we let $\omega \to 0$

We will look in detail at two physically distinct consequences:
1. Two discrete states $\ket{i}$ and $\ket{f}$ in a two level system with a t-dependent Hamiltonian.
2. A discrete level $\ket{i}$ together with a continuum of final states
	$\implies$ Fermi's golden rule.