## Recap Dipole Selection Rule:

Towards the end of last lecture, we got the following 
$$
\bra{\alpha_{2}, j_{2},m_{2}}  z \ket{\alpha_{1},j_{1},m_{1}} = 0 \quad \text{unless} \quad j_{2=}
\begin{cases}
j_{1}+1 \\
j_{1} \\
j_{1} -1
\end{cases}

\quad \text{and} \quad m_{2}=m_{1} \tag{1}
$$

and if we do this explicitly, we will get the following integral 
$$
\int_{0}^{2\pi} \int_{-1}^{1} Y^{*}_{l_{2}m_{2}}(\theta,\phi) \cos \theta Y_{l_{1},m_{1}} \, d(\cos \theta)  \, d\phi \tag{2}
$$
___
Suppose we treat $z = r\cos \theta \sim \cos \theta \sim Y_{l=1}$ is an angular momentum $l=1$ object.  Therefore, $z Y_{l_{1},m_{1}} \sim Y_{1} Y_{l_{1},m_{1}}$. We can treat this as if we are adding angular momentum, and get $l_{1}-1 ,l_{1},l_{1}+1$  according to the "addition" of angular momentum, and hence we have the condition of $j$ in $(1)$.

Aside from $\hat{z}$ operators, we also have $\hat{x}$ and $\hat{y}$. They have the following selection rule:
$$
\begin{align}
\bra{\alpha_{2} l_{2}m_{2}} \hat{x} \ket{\alpha_{1} l_{1}m_{1}}  & = 0   \\

\bra{\alpha_{2} l_{2}m_{2}} \hat{y} \ket{\alpha_{1} l_{1}m_{1}}  & = 0  
\end{align}
\quad \text{unless} \quad l_{2} =
\begin{cases}
l_{2} = l_{1}-1 \\
l_{1} \\
l_{1}+1
\end{cases}
\quad
\text{and}
\quad
m_{2}=
\begin{cases} 
m_{1}+1 \\
m_{1}-1
\end{cases} \tag{3}
$$
We can check this by looking at the functional form, but the reason why the condition for $m$ changes is because the operators $\hat{x}, \hat{y}$ does have $\phi$ dependence.


Note that because the position operators have odd parity, and ket $\ket{\alpha_{1},l_{1},m_{1}}$ has parity $(-1)^{l_{1}}$ , and bra $\bra{\alpha_{2},l_{2},m_{2}}$ has parity $(-1)^{l}$, we must have:

$$
\begin{align}
\bra{\text{even}} \vec{R} \ket{\text{even}}  & = 0  \\
\bra{\text{odd}}  \vec{R} \ket{\text{odd}}  & =0  \\
\implies l_{1}  & \neq l_{2}
\end{align} \tag{4}
$$
Note that this will modify condition $(3)$, and nothing is wrong because condition $(3)$ only consider the rotational symmetry, where condition $(4)$ considers the parity condition. Consequently, condition $(4)$ will modify condition $(2)$ in the sense that $l_{2}$ can no longer equal to $l_{1}$.

## Quantize the EM Field

### Motivation:
Note that so far, we have only consider the quantize photon, but we have treated the EM field classically via using $\vec{A}$ and $\vec{\Phi}$. In the case of resonance, we  cannot explain the fact that an atom starting in an excited state, which is an eigenstate of $H$. Therefore, technically the excited state is stable. However this is not what we see- excited states have a life-time until it decays into the ground state even in the absence of any EM field.

This means because of energy conservation, we will need to create a photon out of nothing. Therefore, this gives us the motivation to quantize the EM field for this behavior to happen. 

Note that this decay behavior spontaneous, and this is because the entropy of a photon + an electron in the ground state is higher than a single electron in the excited state, and the second law of thermodynamics says this would be spontaneous!

### Deduction (Sakurai, p. 472 ff)

Setup: 
We have classical EM radiation in a $L^{3}$ box
No source: $\rho =0$, $\vec{j}=0$
Solve the free space Maxwell equation in this box with the gauge
$$
\begin{align}
\vec{\nabla} \cdot \vec{A}  & = 0 \\
\Phi & =0
\end{align}
$$
From classical EM, we know $\vec{A}$ must satisfy the wave equation 
$$
\begin{align}
\nabla^{2} \vec{A} -  & \frac{1}{c^{2}} \frac{\partial^{2} \vec{A}}{\partial t^{2}}  =0 \tag{5}\\
\vec{E}  & =\frac{1}{c} \frac{\partial \vec{A}}{\partial t} \\
\vec{B}  & = \vec{\nabla} \times \vec{A}

\end{align}
$$
The solution to the wave function is 
$$
\vec{A}(\vec{r},t) = \sum_{\vec{k},\alpha}\vec{A}_{\vec{k},\alpha}(\vec{r},t) \quad \text{sum of all the nodes in the box}
$$
where 
$$
\vec{k} = (k_{x},k_{y},k_{z}) = \frac{2\pi}{L}(n_{x},n_{y},n_{z})
$$
and $\alpha$ is the polarization. The components in the sum are:
$$
\vec{A}_{\vec{\vec{k}},\alpha} = \hat{e}_{\vec{k}\alpha}[A_{k \alpha}e^{-i(\omega_{k} t -\vec{k} \cdot \vec{r})}+A^{*}_{k\alpha}e^{i(\omega_{k}t-\vec{k}\cdot \vec{r})}]
$$
(Note that because of this, $\vec{A}_{\vec{k} \alpha} \in \mathbb{R}$ )
When $l\to \infty, \omega_{k} = e |\vec{k}| = ek$.

Because $\vec{\nabla} \cdot \vec{A} = 0 \implies \vec{k} \cdot \vec{A}_{k\alpha}=0$ and $\vec{k} \cdot \vec{e}_{\vec{k} \alpha}=0$. This is saying $\hat{e}_{\vec{k} \alpha} \perp \vec{k}$, meaning that we have a transverse wave, which has two planes satisfying he perpendicular condition.

Finally, in classical EM, the energy in the Em field is:
$$
\epsilon = 8\pi \int [|\vec{E}(\vec{r},t)|^{2}+| \vec{B}(\vec{r},t)|^{2}] \, d^3r 
$$
If we restrict ourselves into a given mode, so we only consider one $\vec{A}_{\vec{k},\alpha}$ satisfying (5), we have the case(check) of each node having like a harmonic oscillator.

After skipping some algebra in classical EM (See Sakurai), we can express $\epsilon$ in terms of $A_{k,\alpha}$ and $A^{*}_{k,\alpha}$. Skipping some algebra, we can get:

$$
\epsilon = \frac{L^{3}}{4\pi} \sum_{\vec{k},\alpha} \left( \frac{\omega_{k}}{c} \right)^{2}[A^{*}_{k\alpha}A_{k\alpha}+A_{k\alpha}A^{*}_{k\alpha}]
$$

