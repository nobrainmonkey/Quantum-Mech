## Recap:
Classical E&M
Solve the wave equation for vector potential in the gauge in a box of size $L^{3}$
$$
\begin{align}
\Phi  & = 0 \\
\vec{\nabla} \cdot \vec{A}  & = 0
\end{align}
$$
implies
$$
\vec{A}(\vec{r},t) = \sum_{\vec{k}, \alpha} = \hat{e}_{\vec{k}, \alpha}[A_{k,\alpha} e^{-i(\omega_{k}t - i \vec{k} \cdot \vec{r})}+A^{*}_{k,\alpha}e^{i(\omega_{k}t-\vec{k}\cdot \vec{r})}] \tag{1}
$$
Where a state $\vec{k},\alpha$ is a mode and $\vec{k} = \frac{2\pi}{L}(n_{x},n_{y},n_{z})$ and $\alpha$ is the transverse polarization.

Note that $\alpha$ is transverse, so the solution $\hat{e} \perp \alpha$ which is apparent in the gauge we chose, but this is a general statement.

Also note that $A_{k,\alpha}$ and $A_{k,\alpha}^{*}$ is nothing but the complex amplitude of their corresponding waves in $(1)$, and because the velocity of EM wave is $c$, we then have $\omega = ck$.

The energy stored in the EM field is (algebra in Sakurai)
$$
\mathbf{E} = \frac{L^{3}}{4\pi}\sum_{\vec{k},\alpha}\left( \frac{\omega_{k}}{c} \right)^{2} (A^{*}_{k,\alpha} A_{k,\alpha} + A_{k,\alpha}A^{*}_{k,\alpha}) \tag{2}
$$
Note that the reason we wrote $A_{k,\alpha}$ in this way is because $A$ will become an operator in QM, and they don't necessarily commute.
___
This is kind of difficult, because we can have an infinite amount of modes $\vec{k}$. We try to convert a classical $\mathbf{E}$ in equation $(2)$ to a quantum Hamiltonian $\mathcal{H}$. Be careful about commutation relation! By doing this, we elevate the constant $A_{k,\alpha}\to \hat{a}_{k,\alpha}$ and $A_{k,\alpha}^{*}\to \hat{a}^{\dagger}_{k,\alpha}$ where $\hat{a},\hat{a}^{\dagger}$ are operators. 

We define a algebra on the operator 
$$
\begin{align}
[\hat{a}_{k,\alpha},\hat{a}^{\dagger}_{k',\alpha'}]  & = \delta_{k,k'} \delta_{\alpha,\alpha'} \\
[\hat{a}_{k,\alpha},\hat{a}_{k',\alpha'}] & = 0 \\
[\hat{a}^{\dagger}_{k,\alpha},\hat{a}^{\dagger}_{k',\alpha'} ] & =0
\end{align} \tag{3}
$$
The intuition of defining such operator is from the raising and lowering operator of the harmonic oscillators.

Now we write down a quantum Hamiltonian that look like $(2)$
$$
\hat{\mathcal{H}} = \sum_{\vec{k},\alpha} \frac{\hbar\omega_{k}}{2}(\hat{a}^{\dagger}_{k,\alpha} \hat{a}_{k,\alpha}+\hat{a}_{k,\alpha}\hat{a}^{\dagger}_{k,\alpha}) \tag{4}
$$
Note the correlation between $(2)$ and $(4)$.

Looking at a specific node, we have, from $(3)$
$$
\begin{align}
a a^{\dagger} - a^{\dagger} a = 1 \\
a a^{\dagger} = 1 + a^{\dagger} a
\end{align}
$$
Using this relation, we can re-write $(4)$ as :
$$
\hat{\mathcal{H}} = \sum_{k,\alpha} = \hbar \omega_{k} \left( \hat{a}^{\dagger}_{k,\alpha}\hat{a}_{k,a}+\frac{1}{2} \right) \tag{5}
$$
Please note the similarity of $(5)$ with the Hamiltonian of a harmonic oscillator. This is saying that each mode $\vec{k},\alpha$ look like a quantum harmonic oscillator with frequency $\omega_{k}$.

___
Note that in order to get the pre-factor of $(4)$, we have replaced the classical object $$A_{k,\alpha}\to \frac{1}{L^{3/2}} \left( \frac{2 \pi \hbar c^{2}}{\omega_{k}} \right)^{1/2} \hat{a}_{k,\alpha}$$
The detail of this is not physically relevant.
___
we can re-write $(4)$ by separating the mode label:
$$
\mathcal{H} = \sum_{\alpha = 1,2,\dots}\sum_{\vec{k}}\left( \hat{a}^{\dagger}_{k,\alpha} \hat{a}_{k,\alpha}+\frac{1}{2} \right) \hbar \omega_{k}
$$
where the two sums still resemble the sum over all modes, but note that because, in quantum harmonic oscillator, we have $\hat{N} = \hat{a}^{\dagger}a$, this means that here, $\hat{a}^{\dagger}_{k,\alpha} \hat{a}_{k,\alpha}$ resembles the number of photons in mode $\vec{k},\alpha$,  the $1/2$ is nothing but the "zero point energy", and the $\hbar \omega_{k}$ is the energy of photon in mode $\vec{k},\alpha$ with $\omega = ck$.

## Vacuum State:
The ground state of $\mathcal{H}$ is called the **vacuum state** $\ket{0}$. Analogous to harmonic oscillator, $\ket{0}$ is defined by the conditions: 
$$
\begin{align}
\hat{a}_{k,\alpha} \ket{0}  & = 0 \\
\implies  \hat{a}^{\dagger}_{k,\alpha} \hat{a}_{k,\alpha} \ket{0}  & =0 \\
\implies  \text{no photons} &\text{in the vacuum}
\end{align}
$$
We can see that $\mathcal{H} \ket{0}= \sum_{\vec{k},\alpha} \frac{1}{2} \hbar \omega_{k} \ket{0}$, but because we have a infinite sum over a value, this indicates that the vacuum has a infinite amount of energy or some constant. We denote this ground state energy $E_{0}$.

Even though this is problematic mathematically, we don't really bother to calculate the ground state energy $E_{0}$ because, when doing the experiment, all we measure is the difference of energy from the ground state.

Now we want to know if there are $\vec{E}, \vec{B}$ in the vacuum. Note that classically, we have 
$$
\begin{align}
\vec{E}  & = -\frac{1}{c} \frac{\partial \vec{A}}{\partial t} \\
\vec{B}  & = \vec{\nabla} \times \vec{A}
\end{align}
$$
where both of these are linear combination of $\hat{a}$ and $a^{\dagger}$ summed over modes. 

If we want 
$$
\braket{ 0}  \vec{E}\ket{0} \quad \text{and} \quad \bra{0} \vec{B} \ket{0} 
$$
we can use the linear combination of 
$$
\bra{0} \hat{a}_{k,\alpha} \ket{0}  \quad \text{and} \quad \bra{0} \hat{a}^{\dagger}_{k,\alpha}\ket{0} 
$$
and realize both of the component will be 0. Therefore, it turns out that 
$$
\bra{0} \vec{E} \ket{0}  = \bra{0} \vec{B} \ket{0} =0
$$
This make sense as, on average, the ground state which is the vacuum state should not have and $\vec{E}$ or $\vec{B}$ field.

But note that 
$$
\bra{0} \vec{E}^{2} \ket{0} \neq 0 \quad \text{and} \quad \bra{0} \vec{B}^{2}\ket{0} \neq 0
$$
This is true be cause when we square them, there will be term like $\hat{a} \hat{a}^{\dagger}$ which has none zero expectation value. This means that there is a fluctuation of $\vec{E}$ and $\vec{B}$ field in vacuum.

Note that this consequence is the same as a harmonic oscillator 
$$
\begin{align}
\bra{0} x \ket{0}  & = 0  \\
\bra{0} x^{2} \ket{0}  & \neq 0
\end{align}
$$
The fact that we have fluctuation of $\vec{E}$ and $\vec{B}$ field in the vacuum ties to the fact that we have none zero vacuum energy $E_{0}$.
___

## Excited states:

In parallel with the harmonic oscillators, we can show that
$$
\ket{\vec{k},\alpha} := \hat{a}^{\dagger}_{\vec{k},\alpha} \ket{0} 
$$
is an eigenstate of $\mathcal{H}$. We can check that 
$$
\mathcal{H} \ket{\vec{k},\alpha} = \hbar \omega_{k} \ket{\vec{k},\alpha}  
$$
The reader should **check this** in detail!

We call $\ket{\vec{k},\alpha}$ the 1- photon state with a photon of energy $h \omega_{k} = \hbar ck$ in the mode $\vec{k},\alpha$.
Note that this is a single quantum excitation of a EM field.

We can discuss the momentum of a photon:
Intuitively, we already know that $E = \hbar \omega_{k}$, so the momentum should be $\hbar \vec{k}$.

Classically, the momentum $\vec{p}_{cl} = \frac{1}{4\pi c} \int \vec{E} \times \vec{B} \, d^3r$. If we were to make $\vec{p}_{cl}$ to be a operator $\hat{p}$, and we can make $\vec{E}, \vec{B}$ to be expressed in $\vec{A},$ which we can quantize using $\hat{a},\hat{a}^{\dagger}$. After a huge amount of algebra, we reach a quantum answer that the quantum momentum:

$$
\hat{p} = \sum_{\vec{k},\alpha} \hbar \vec{k}\  \hat{a}^{\dagger}_{k,\alpha} \hat{a}_{k,\alpha}
$$
which implies 
$$
\hat{p} \ket{\vec{k},\alpha} = \hbar \vec{k} \ket{k,\alpha}  
$$

Now we can calculate the mass of photon 
$$
\begin{align}
E = \hbar ck \quad \text{and} \quad E^{2} = p^{2}c^{2}+m^{2}c^{4} \\
p = \hbar k \implies m^{2}c^{4}=0 \implies m_{\gamma}=0
\end{align}
$$
We can also calculate the spin (angular momentum) of a photon.
One can start with the classical result, which is not so familiar to many, so, instead, let us use a plausibility argument that the wave equation in coordinate space is 
$$
\braket{ \vec{r} | \vec{k}\alpha } =\frac{e^{i \vec{k} \cdot \vec{r}}}{L^{3/2}} \hat{e}_{\vec{k},\alpha}
$$
where $\hat{e}_{\vec{k},\alpha}$ is the polarization vector. This implies angular momentum $S = 1 \hbar$, so one might propose that we have 3 $S_{z}$ state $S_{z} = 1, 0, -1$.

It turns out that the photon only has $S_{z} = \pm 1$ states (right/left polarization). The reason why we only have two sates is because we have two transverse polarization. At $v=c$, we can never get to the rest frame of $v=c$. Therefore, we could never get to the longitudinal frame which is traveling at the speed of light.