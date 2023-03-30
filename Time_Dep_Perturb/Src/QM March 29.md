## Recap:
$\ket{\psi(0)}=\ket{i}$
$H = H_{0}+ H_{1}(t) \implies \ket{\psi(t)}=\sum_{f}a_{f}(t)e^{-i \omega_{f}t} \ket{ f}$
where we have computed $a_{f}(t)$ using first order time-dependent perturb theory, and for $i \neq f$ 
$$
P_{i\to f}(t) = \lvert \braket{ f | \psi(t }  \rvert ^{2}  = \frac{\lvert V_{fi} \rvert^{2} }{\hbar^{2}} \left[ \left( \frac{\sin(\omega_{fi}-\omega)t/ 2}{(\omega_{fi}-\omega) / 2} \right) \right]^{2} \tag{1} 
$$
for $H_{1}(t)= 2\hat{V} \cos \omega t, \hbar \omega_{fi}=E_{f}-E_{i}, \text{and} \ V_{fi}=\bra{f} \hat{V}\ket{i}$. 
___
## Fermi's Golden Rule:
Let us look at large $t$ behavior of $P_{i\to f}(t)$, and claim that equation $(1)$ at large $t$, we have 
$$
\left( \frac{\sin(\omega_{fi}-\omega)t/ 2}{(\omega_{fi}-\omega) / 2} \right) ^{2} \to_{t \  \text{large}} 2\pi t \delta(\omega-\omega_{fi}) \tag{2} 
$$
We check that 
1. Equation $(2) \geq 0$
2. Width of $(2) \sim \frac{1}{t}$
3. Height of $(2) \sim t^{2}$  
4. $\int_{-\infty}^{\infty} \frac{\sin^{2}x}{x^{2}} \, d x =\pi$
Using these and equation$(2)$, we conclude that 
$$
\lim_{ t \to \infty } \frac{P_{i \to f}(t)}{t}=\frac{2\pi}{\hbar^{2}} \lvert \bra{f} V \ket{i}  \rvert^{2} \delta(\omega-\omega_{fi}) \tag{3} 
$$
The physical interpretation of $(3)$ is the rate of making transition from $\ket{i}\to \ket{f},$ denote as 
$$\Gamma_{i\to f} = \frac{2\pi}{\hbar}\lvert \bra{f}V \ket{i} \rvert^{2} \delta(E-E_{f}+E_{i}) \tag{4} $$
where $(4)$ is called the **Fermi's golden rule.**

Note that the delta function equation $(4)$ represents a concentration of energy. This result is very satisfactory, but in the case of a single state of $\ket{f}$, it is strange that $\Gamma_{i\to f}$ is either zero or infinity.

To reconcile with this strange behavior, we now consider $\ket{i}\to \text{continium of final states} \ \ket{f}$ where we apply $(4)$ to every single final state $\ket{f}$. 

Therefore, we need to sum these different final states with a density of states $\rho(E_{f})$. Under these condition, we should have 

$$
\Gamma = \sum_{f} \Gamma_{i\to f} \equiv \int \rho(E_{f}) \frac{2\pi}{\hbar} \lvert \bra{f} V \ket{i}  \rvert^{2}\delta(\hbar \omega-E_{f} +E_{i})  \, dE_{f}  \tag{5} 
$$
Or we can write this as 
$$
\Gamma = \frac{2\pi}{\hbar}\lvert \bra{f} V \ket{i}  \rvert ^{2}  \rho(E_{f}) \rvert_{E_{f}=E_{i}+\hbar \omega}  \tag{6} 
$$
Note that equation $(6)$ is a more physical form of Fermi's golden rule.

We will skip the validity of when to applying Fermi's golden rule.
___
### Example: Fermi's golden rule $\to$ Born's approximation

$\ket{i}= \text{plane wave}$
Physically, what we will do it to "turn on" the scattering potential at $t=0$ and then applying Fermi's golden rule. This means that:
$V(t)$ which causes scattering into various $\ket{f}$.
$\braket{ \vec{r} | i } = \frac{1}{L^{3/2}}e^{i \vec{k}_{i} \cdot \vec{r}}$ which is a $3-d$ plane wave.
$\braket{ \vec{r} | f }=\frac{1}{L^{3/2}e^{i \vec{k}_{f} \cdot \vec{r}}}$
Therefore, we have:
$$
\begin{align}
\bra{f} \hat{V} \ket{i}   & = \int \int \braket{ f | \vec{r}' } \bra{\vec{r}'} \hat{V} \ket{\vec{r}} \braket{\vec{r}  |i  }    \, d^3 \vec{r}'  \, d^3 \vec{r} \\
&=\frac{1}{L^{3}}\int e^{-i (\vec{k}_{f} - \vec{k}_{i}) \cdot \vec{r}} \, d^3 \vec{r}  \\
& = \frac{1}{L^{3}} V(\vec{q})|_{\text{F.T.}}
\end{align} \tag{7} 
 
$$
We note that in 3-d, each state occupy a space $\hbar^{3} \left( \frac{2\pi}{L} \right)^{3}$ in momentum space. Therefore, we must have the number of states in a box of volume $L^{3}$ that lie in the region $d^{3} \vec{p}$ about $\vec{p}$ is 
$$
\begin{align}
N&=\frac{d^{3}\vec{p}}{(2 \pi \hbar)^{3}}L^{3} \\
&= \frac{L^{3}p^{2} dp \ d\Omega_{\hat{p}}}{(2\pi \hbar )^{3}} \\
&\equiv \rho(E) dE \ d\Omega_{\hat{p}}
\end{align} \tag{8} 
$$
where $\rho(E) dE$ is the number of states (for a plane wave) in a box of volume $L^3$ that lie in the energy range $(E,E+dE)$.

from equation$(8)$, we find:

$$
\rho(E) = \frac{L^{3}p^{2}}{(2\pi \hbar)^{3}} \frac{dp}{dE} \tag{9} 
$$
For free particle solution, we use $E = \frac{p^{2}}{2m}$ for equation $(8)$ and found that 
$$
\rho(E) \propto \sqrt{ E } 
$$
Note that if we combine equation$(8)$ and equation$(9)$ to equation $(6)$, we can calculate $\Gamma$

Recall that the cross section $\sigma(\theta) = \frac{\Gamma}{J_{inc}},  \Gamma\sim \frac{2\pi}{\hbar} \lvert V(\vec{q}) \rvert^{2} \rho(E_{f}), \text{and} \ J_{inc} = \frac{1}{L^{3}}\hbar \frac{k_{i}}{m}$.

Recall that $\lvert \vec{k}_{f} \rvert = \lvert \vec{k} \rvert_{i}=k$, and $q = 2k \sin(\frac{\theta}{2})$ where $q = \lvert \vec{k}_{f}- \vec{k}_{i} \rvert$











