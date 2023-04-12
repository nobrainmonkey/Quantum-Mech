## Recap: Photoelectric effect 
We have:
$$
\begin{align}
\ket{i}  & = \text{g.s. of H atom with } \psi_{100} \\
\ket{f}  & =\text{plane wave with momentum } \vec{p}_{f}=h \vec{k}_{f}
\end{align}
$$
Note that since we want to ignore the perturbation from the proton, we require $\hbar \omega = E_{f}- E_{i}\gg \text{Ry}=13.6 \text{eV}$ .

We have the Hamiltonian:
$$
\begin{align}
H_{0} & =\frac{p^{2}}{2m}+V(r) \quad \text{hydrogen atom} \\
H_{1} & = \frac{e}{mc}\vec{A} \cdot \vec{p} = \frac{e}{mc} \frac{\vec{A}_{0}}{2}(e^{i(\vec{k} \cdot \vec{r} - \omega t)}+e^{-i(i \vec{k}\cdot r- \omega t)}) \quad A =A_{0}\cos(\vec{k}\cdot \vec{r} - \omega t) \ \\
\end{align}
$$
With the following gauge:
$$
\begin{align}
\vec{\nabla} \cdot \vec{A} = \Phi=0
\end{align}
$$
___
Because 
$$
\hbar \omega = E_{f} - E_{i} >0
$$
on resonance only the $e^{- i \omega t}$ piece of $H_{1}$ will contribute (Recall: it leads to the resonant denominator $\frac{1}{\omega - \omega_{fi}}$ in the degenerate perturbation theory).

Therefore, we can just focus on 
$$
H_{1}\to \frac{e}{2mc} e^{i (\vec{k} \cdot \vec{r} - \omega t)}\vec{A}_{0} \cdot \vec{p}
$$
We can calculate the matrix element 
$$
\bra{f}  H_{1}\ket{i}  \sim \int e^{- i \vec{k}_{f} \cdot \vec{r}} e^{i \vec{k} \cdot \vec{r}}  \vec{A}_{0} \cdot (- i \hbar \vec{\nabla})e^{-r/a_{0}}\, d^3 \vec{r} 
$$
Note that:
$$
\begin{align}
 & \text{energy of light wave \quad} \hbar \omega  \sim \# \frac{e^{2}}{a_{0} c} \quad \text{where \# is large}  \\
 & \text{momentum of }e^{-} \text{ inside the atom} \quad p   \sim \frac{\hbar}{a_{0}}
\end{align}
$$
Therefore, we have 
$$
\frac{(hk)_{\text{light}}}{(p)_{\text{electron}}} \sim \# \frac{e^{2}}{hc} \sim \frac{\#}{137} \ll 1
$$
This means that we are working in the regime that the momentum of light which is not orders of magnitude larger. In fact, it is likely that the photon energy is only about 5-10 times larger.

Therefore, we will ignore  $(hk)_{\text{light}}$ relative to $(p)_{\text{atom}}$. This justify:
$$
\frac{\text{Zeeman}}{\text{orbital}} \sim \frac{\left\langle  \frac{e}{2mc} \vec{S} \cdot \vec{B}  \right\rangle}{\left\langle  \frac{e}{mc} \vec{A} \cdot \vec{p} \right\rangle } = \frac{\langle  \hbar \vec{\sigma} \cdot (\vec{\nabla} \vec{\times}A) \rangle }{\langle \vec{A}\cdot \vec{p}\rangle } \sim \frac{(\hbar k)_{\text{light}}}{(p)_{\text{electron}}} \ll 1
$$
This means that we can ignore the spin interaction as it is small compared to the momentum of the electron!


In the matrix element:
$$
\begin{align}
\int  \, d^3 \vec{r} \quad \text{only } r & \leq a_{0} \ \text{contribute to the term } e^{-r/a_{0}} \\
(\hbar k)_{\text{light}}  & \ll (p)_{\text{electron}} ~ \frac{\hbar}{a_{0}} \to k a_{0} \ll 1 \to \lambda\gg a_{0} 

\end{align}
$$
Because of this , we can use $e^{ikr} \approx 1$ as our wavelength if much larger than $a_{0}$ inside the integral. This is called the **electric dipole approximation.**

Now, we can evaluate the integral in $\bra{f}H_{1}\ket{i}$
$$
\begin{align}
&e^{i \vec{k}\cdot \vec{r}} \approx 1  \\
&\text{ Do integration by parts so } (-i\hbar \vec{\nabla})(e^{-i \vec{p}_{f} \cdot \vec{r} / \hbar}) \text{ and get}
\end{align}
$$
$$
\begin{align}
- \vec{A}_{0} \cdot \vec{p}_{f} &\int e^{-i \vec{k}_{f} \cdot \vec{r}}e^{-r/a_{0}} \, d^3 \vec{r}  \\
&\int \int \int r^{2} \cos \theta e^{- i k_{f} r \cos \theta} e^{-r/a_{0}} \, d\phi  \, d\theta  \, dr 
\end{align}
$$
The details of this integral is page 504 Shankar. It is a pretty simple integral.

The final answer is 
$$
\propto \frac{1}{[1+ (k_{f}a_{0})^{2}]^{2}} = \left( 8 \frac{\pi}{a_{0}} \right) \frac{1}{\left[ \frac{1}{a_{0}^{2}} + k_{f}^{2}\right]^{2}}
$$
To complete the golden rule calculation,we also need density of state $\rho(E_{f})$

$$
\rho(E_{f}) = \frac{L^{3}}{(2\pi \hbar)^{3}}m p_{f} \leftarrow \text{exactly what we calculated before }
$$
Combining everything together and apply Fermi's golden rule, we get the rate of transition from $\ket{i}\to \ket{f}$ within a solid angle $d \Omega$:

$$
\begin{align}
\Gamma  & =  \frac{2\pi}{\hbar} |\braket{ f} H_{1} \ket{i} | ^{2} \rho(E_{f})    \\
	 & =\frac{2\pi}{\hbar} \left( \frac{e}{2mc}^{2} \right) \frac{1}{L^{3}}(\vec{A}_{0} \cdot \vec{p})^{2} \frac{64 \pi^{2}}{a_{0}^{3}} \frac{1}{\left[ \frac{1}{a_{0}^{2}} +k_{f}^{2} \right]^{4}}  \frac{L^{3} m p_{f}}{(2 \pi \hbar)^{3}}
\end{align}
$$
Note that $(\vec{A}_{0} \cdot \vec{p}_{f})^{2} = |A_{0}|^{2} p_{f}^{2} \cos^{2} \theta$ where $\theta$ is the angle between $\vec{A}_{0}$ and $\vec{p}$.

Now we need $J_{inc}$ to calculate the cross section. Note that $J_{inc}$ should be the probability density current for the photon. Using the pointing vector, the incident beam has an energy per unit time per unit area = $\frac{\omega^{2}}{8 \pi c} |\vec{A}_{0}|^{2}$. 

Therefore, the number of photons is simply $\frac{\omega^{2}}{8 \pi c} |\vec{A}_{0}|^{2} \frac{1}{\hbar \omega} = \frac{\omega |\vec{A}_{0}|^{2}}{8 \pi c \hbar}$.

We finally assemble everything and calculate the cross section 
$$
\begin{align}
\sigma(\theta)  & = \frac{8 \pi \hbar c}{\omega |\vec{A}_{0}|^{2}} \Gamma \\
\sigma(\theta) & = \frac{32 a_{0}^{3} e^{2}p_{f}^{3}\cos^{2}\theta}{m \omega c \hbar^{3}\left[ 1+\left( \frac{p_{f}a_{0}}{\hbar} \right)^{2} \right]^{4}}

\end{align}
$$

Next time:
1. Analyze this awful answer
