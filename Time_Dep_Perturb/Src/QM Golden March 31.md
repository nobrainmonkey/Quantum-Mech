## Recap:

We have derived **Fermi's golden rule** which says the transition rate from an initial state $\ket{i}$ to a final state $\ket{f}$ is:

$$
\Gamma_{i\to f} = \frac{2\pi}{\hbar} | \bra{ f} \hat{V} \ket{i}  | ^{2}\delta(h \omega - E_{f} +E_{i}) \tag{1}
$$
or the rate for all finate state $\ket{f}$ is:

$$
\Gamma = \sum_{f}\Gamma_{i\to f} =\frac{2\pi}{\hbar} |\bra{ f} \hat{V}\ket{i}  | ^{2} \rho(E_{f})  \tag{2}
$$
where $\rho(E)$ is the density of state at energy $E$.

We also tried to **Retrieve the Born Approximation**. We have that 

$$
\begin{align}
\braket{ \vec{r} | i }  & = \frac{1}{L^{3/2}} e^{i \vec{k}_{i} \cdot \vec{r}} \\
\braket{ \vec{r} | f }  & =\frac{1}{L^{3/2}}e^{i \vec{k}_{f} \cdot \vec{r}}
\end{align}
$$
define $\vec{q}=\vec{k}_{f}-\vec{k}_{i}=2k \sin \frac{\theta}{2}$.

We also have:
$$
\braket{ f} \hat{V} \ket{i} = \frac{1}{L^{3}}\int e^{-i (\vec{k}_{f}-\vec{k}_{i}) \cdot \vec{r}} V(r) \, d^3 \vec{r} = V(\vec{q}) | _{\text{F.T.}} 
$$
For the density of state, we have 
$$
\rho(E) = \frac{dN}{d E \ d\Omega_{\hat{p}}} 
$$
where 
$$
dN = L^{3} \frac{p^{2}dp \ d\Omega}{(2 \pi \hbar)^{3}}
$$
Therefore:
$$
\rho(E) = \frac{L^{3}p^{2}}{(2\pi \hbar)^{3}} \frac{dp}{dE}
$$
but we know that $E = \frac{p^{2}}{2m}\implies \frac{dE}{dp}= \frac{p}{m}$ 
This finally gives:
$$
\rho(E) = L^{3} \frac{mp}{(2\pi \hbar)^{3}}
$$
Using equation $(2)$, we have 
$$
\Gamma = \left( \frac{2\pi}{\hbar} \right)^{3} \frac{1}{L^{6}} | V(\hat{q})|^{2} \frac{L^{3}m \hbar k_{f}}{(2 \pi \hbar)^{3}}
$$

and we have $\sigma(\theta) = \frac{\Gamma}{|\vec{J}_{inc}|}$ where $\vec{J}_{inc} = \frac{1}{L^{3}} \frac{\hbar \vec{k}_{i}}{m}$ (check this using probability current).

Combining everything (check this)
$$
\sigma(\theta) = \frac{\Gamma}{| \vec{J}_{inc}|} = \frac{m^{2}}{(2\pi)^{2}\hbar^{4}} \left\lvert \int e^{i \vec{q} \cdot \vec{r}} V(r) \, d^{3} \vec{r}\right\rvert^{2} 
$$

in which we get back to **Born's approximation.**

___
## Interaction Between Radiation and Matter

We look at a restricted domain where matter is treated using **QM**. To begin our analysis, we will start by treating the radiation **classically.** 

Therefore, we will specify our radiation as: 
$$
\begin{align}
\vec{E} & = - \vec{\nabla}\Phi - \frac{1}{c} \frac{\partial \vec{A}}{\partial t} \\
\vec{B}  & =\vec{\nabla} \vec{\times}A
\end{align}
$$
Then, for a charged particle with charge $q=-e$ (e.g. electron), we have the following Hamiltonian:

$$
H = \frac{1}{2m}\left( \vec{p} + \frac{e}{c} \vec{A} \right)^{2} - e\Phi + V(r)
$$
Note that the above Hamiltonian did not include the spin of the electron. This means we ignore the Zeeman effect $\propto - \vec{\sigma} \cdot \vec{B}$. We will justify later why this is OK.

Note that because we use $\vec{A}$ and $\Phi$ to represent the radiation, then we have to choose a gauge for the fields. We generally choose the following gauge:
$$
\begin{align}
\vec{\nabla} \cdot\vec{A}  & = 0 \\
\Phi  & =0
\end{align}
$$
Note that we set $\Phi=0$, so we do a small perturbation in terms of $\vec{A}$ to our Hamiltonian. Therefore, we expand the term $\left( \vec{p}+ \frac{e}{c} \vec{A} \right)^{2}$ in terms of $\vec{A}.$

$$
\begin{align}
\left( \vec{p} + \frac{e}{c} \vec{A}  \right)^{2}  & = \left( - i \hbar \vec{\nabla} + \frac{e}{c} \vec{A} \right)^{2} \\
\end{align}
$$
We have the following expansion:
0th order $\to \frac{\vec{p}^{2}}{2m} \psi= -\frac{\hbar^{2}}{2m} \nabla^{2}\psi$
1st order $\to \frac{e}{2mc}(-i \hbar)(\vec{A} \cdot \vec{\nabla} + \vec{\nabla} \cdot \vec{A})\psi= 2 \vec{A} \cdot \vec{\nabla} \psi$  for our choice of gauge that $\vec{\nabla} \cdot A =0$.

Therefore, we have 
$$
H = H_{0} + H_{1}
$$
where 
$$
\begin{align}
H_{0}  & =\frac{p^{2}}{2m}+V(r) \\
H_{1} & =\frac{e}{mc}\vec{A} \cdot p
\end{align}
$$
___
### Photoelectric Effect

With this setup, we can talk about the **photoelectric effect** of hydrogen.

Note that the hydrogen atom has discrete bound state for $E <0$ and continuous unbounded state for $E>0$. 
We then consider a state starting from $\ket{i}$ a bound state to $\ket{f}$ a continuous state.

Note that the means for $\ket{i}\to \ket{f}$ is by absorbing a "photon." However, since we are considering the radiation to be **classically**, the means of the transition is actually a time-dependent perturbation:

$$
E_{f} =E_{i} + \hbar \omega
$$
where $\omega$ coming from the $e^{-i \omega t}$ dependence of the $\vec{A}$ field.

To simplify matters, we assume that
$$
\hbar \omega = E_{f}-E_{i} \gg 13.6 \text{eV}
$$
We make this assumptions because we want to make our final state $\ket{f}$ to be only slightly (or not at all in limiting case) of the proton. Therefore, we need much more energy to put our final state $\ket{f}$ into a high energy state.

Because of this, our final state will just be a plane wave due to it not perturbed by the proton. Therefore, we have:
$$
\braket{ \vec{r} | f } = \frac{1}{L^{3/2}}e^{i \vec{p}_{f} \cdot \vec{r} / \hbar}
$$
and the initial state $\ket{i}$ is just the hydrogen wave function ground state:
$$
\braket{ \vec{r} | i } = \frac{1}{\sqrt{ \pi a_{0}^{3} }}e^{-r/a_{0}}
$$
Next, we will then want to calculate:
1. $\bra{f} H_{1}\ket{i}$
2. $\rho(E_{f})$
3. apply golden rule.

