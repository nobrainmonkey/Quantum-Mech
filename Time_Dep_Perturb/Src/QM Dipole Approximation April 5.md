## Recap:
We found the photo-ionization cross-section 
$$
\sigma(\theta) = \frac{\frac{32 a_{0}^{3} e^{2} p_{f}^{3}}{m \omega e \hbar^{3}}(\cos^{2} \theta)}{\left[ 1 + (\frac{p_{f}a_{0}}{\hbar})^{2} \right]^{4}} \tag{1}
$$
___
### Dimensional Analysis:
Note that the we can re-write equation $(1)$ as (ignoring constant and dimensional less quantities)
$$
\frac{e^{2}}{\hbar c} a_{0}^{2} \frac{p_{f}a_{0}}{\hbar} \left( \frac{E_{f}}{\hbar \omega} \right)  \tag{2}
$$
Note that equation (2) written in this way clearly has cross-section unit $L^{3}$ .

### Angle part (from last lecture)
We know that 
$$
\cos ^{2 } \theta \sim (\vec{A}_{0} \cdot \vec{p}_{f})^{2} \tag{3}
$$
where the direction of $\vec{A}_{0}$ determines the polarization of the $\vec{E}$ field because $\vec{E} = \frac{1}{c}\frac{\partial \vec{A}}{\partial t}$ . This means that equation $(3)$ is maximized when $\vec{p}_{f} \mid\mid \vec{E}$, and it is min when $\vec{p}_{f} \perp \vec{E}$.

### Denominator
Note that the denominator of $(1)$ 
$$
\frac{1}{\left[ 1 + \left( \frac{p_{f} a_{0}}{\hbar} \right)^{2} \right]^{4}}  \sim | \braket{ \vec{p}_{f} | \psi_{100} } |^{2}
$$
This is because 
$$
\begin{align}
&\bra{\vec{p}_{f}} H_{1} \ket{\psi_{100}} \\
&\sim  \vec{A}_{0} \cdot \bra{\vec{p}_{f}} \vec{\nabla} \ket{\psi_{100}} \\
& \sim \vec{A}_{0} \vec{p}_{f} \braket{ \vec{p}_{f} |\psi_{100}  }     \\
\implies & \braket{ \vec{p}_{f} | \psi_{100} } \sim \frac{1}{\left[ 1+ \left( \frac{p_{f}a_{0}}{\hbar} \right)^{2} \right]^{2}} 
\end{align}
$$
Note that the overlap integral between $\braket{ \vec{p} | \psi_{100} }$ is nothing but imaging the ground state wave function in $\vec{p}$ space. Specifically, we are probing $\vec{p}_{f}$ in $\psi_{100}$.

___
## Electric Dipole Approximation
We have the set-up
$$
\begin{align}
\vec{E} = -\frac{1}{c} \frac{\partial \vec{A}}{\partial t} = \frac{i\omega}{c}\vec{A}_{0}e^{- i \omega t} e^{ i \vec{k} \cdot \vec{r}} + \text{c.c} \tag{4}
\end{align}
$$
where the absorption $e^{-i \omega t}$ dominates, and $e^{i \vec{k} \cdot \vec{r}} \approx 1$  because $\lambda = \frac{2\pi}{k} \gg a_{0}$ 

This indicates that equation $(4)$ is almost spatially invariant as the main contribution comes from resonant absorption.
Because $\vec{E}$ couples to the electric dipole $|e| \vec{R}$ where $\vec{R}$ is the position vector of $e^{-}$  , we have:
$$
H_{\text{dip}} = - |e| \vec{R} \cdot \vec{E} = - i \frac{\omega}{2c} |e| \vec{A}_{0} \cdot \vec{R} e^{- i \omega t} \tag{5}
$$
However, what we did instead for the dipole approximation is 
$$
H_{1} = \frac{-|e|}{2mc} \vec{A}_{0} \cdot \vec{p} e^{- i \omega t} \tag{6}
$$
This is rather strange,  because equation $(6)$ is independent of the position vector $\vec{R}$, but equation $(5)$ couples vector potentials to position. This is what we are trying to understand.

Let us start considering this with a unperturbed hydrogen atom $H_{0} = \frac{p^{2}}{2m} + V(R)$
We observe that 
$$
[\vec{R}, H_{0}] = \frac{i\hbar}{m} \vec{p} \tag{7}
$$
Note that our because equation $(7)$ relate $\vec{R}$ and $\vec{p}$, let us start from this. Sand-witching  equation $(7)$ gets:

$$
\begin{align}
\braket{ f} [\vec{R}, H_{0}] \ket{i}  & = \frac{i\hbar}{m}\bra{f} \vec{p} \ket{i}   \\
\implies -(E_{f}- E_{i}) \bra{f} \vec{R} \ket{i} & = \frac{i\hbar}{m}\bra{f} \vec{p} \ket{i}   \\
\implies \bra{f} H_{1} \ket{i}   & = \frac{- | e| }{2mc} \vec{A}_{0} \cdot \braket{ f}  \vec{p} \ket{i}  e^{- i \omega t} \\
& = \frac{-  | e| }{2mc}(i m \omega_{fi}) \vec{A}_{0} \cdot \bra{f} \vec{R} \ket{i} e^{- i \omega t} \\
& = \frac{\omega_{fi}}{\omega} \bra{f} H_{dip} \ket{i} 
\end{align}

$$
Because we are near resonance, so we have $\omega \approx \omega_{fi}$, we have $H_{1} \approx H_{dip}$.

## Selection Rules:
(pp 458-459 Shankar in time-independent P.T.)

Q. When does $\bra{f} H_{1}\ket{i} = 0$ for a given perturbation $H_{1}$?

Let us exploit symmetry. First, symmetry is something that **commutes with the Hamiltonian**, let's call this symmetry operator $\Lambda$.By the definition of symmetry, we have 
$$
\begin{align}
[\Lambda, H_{0}] = [\Lambda, H_{1}] =  [\Lambda, H]=0
\end{align}
$$
and let us consider the eigenstates of $\Lambda$
$$
\Lambda \ket{\alpha_{i}, \lambda_{i}}  = \lambda_{i} \ket{a_{i},\lambda_{i}} 
$$
this implies:
$$
\bra{\alpha_{2}, \lambda_{2}} H_{1} \ket{\alpha_{1},\lambda_{1}} = 0 \quad \text{unless} \quad \lambda_{2} = \lambda_{1}  \tag{8}
$$
### Proof of $(8)$
$$
\begin{align}
\bra{\alpha_{2} ,\lambda_{2}}[\Lambda,H_{1}] \ket{\alpha_{1},\lambda_{1}}  & = 0 \\
(\lambda_{2}-\lambda_{1}) \bra{\alpha_{2},\lambda_{2}}H_{1} \ket{\alpha_{1},\lambda_{1}}  & =0  \\
\text{if} \quad \lambda_{2} \neq \lambda_{1} \implies   \bra{\alpha_{2},\lambda_{2}}H_{1}\ket{\alpha_{1},\lambda_{1}} & = 0  
\end{align}
$$
### Example 1: Parity
Let $\Lambda = \text{parity}$  
if $[H_{1},\Lambda] = 0$, then:
$$
\begin{align}
\bra{\text{odd}} H_{1} \ket{\text{even}}  & = 0  \\
\bra{\text{even}} H_{1} \ket{\text{odd}}  & =0  
\end{align}
$$
In this case, we cut the amount of calculation by a factor of 2!

### Example 2: Dipole Selection Rule
Let us use angular momentum states:
$$
\bra{\alpha_{2}, j_{2},m_{2}}  z \ket{\alpha_{1},j_{1},m_{1}} = 0 \quad \text{unless} \quad j_{2=}
\begin{cases}
j_{1}+1 \\
j_{1} \\
j_{1} -1
\end{cases}

\quad \text{and} \quad m_{2}=m_{1}
$$
Let us focus on a special case where $\vec{S}=0$, this gives $\vec{J} = \vec{L}$

Then, the matrix element becomes:
$$
\int_{0}^{2\pi} \int_{-1}^{1} Y^{*}_{l_{2}m_{2}}(\theta,\phi) \cos \theta Y_{l_{1},m_{1}} \, d(\cos \theta)  \, d\phi
$$
Note that the condition for $m_{2}=m_{1}$ is clear, as the $e^{-i m_{2} \phi}$ and $e^{- m_{1} \phi}$ should cancel each other.



