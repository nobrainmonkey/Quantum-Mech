## Recap:

If we have a Hamiltonian $H(t)$, we first diagonalize it and get instantaneous eigenstates $H(t) \psi_{n}(t) = E_{n} \psi_{n}(t)$ . Usually we use a path $\vec{R}(t)$ to represent such time dependence. Using the fact that $\dot{H}$ is small, we can write down an approximation 

$$
\psi_{n}(\vec{R}(t)) e^{i \theta_{n}(t)}e^{i \delta_{m}(t)} \tag{1} 
$$
where $\theta_{n}(t)$ is the dynamic phase that come from $H(t)$, and we have the equation for the geometric phase $\delta_{n}$:

$$
\delta_{n}(t) = i \int_{\vec{R}_{i}}^{\vec{R}_{f}} \braket{ \psi_{n}(\vec{R}) | \nabla_{R} \psi_{n}(\vec{R}) }  \, \vec{R}   \tag{2} 
$$
And if we have a closed loop where $\vec{R}_{i} = \vec{R}_{f}$ , we have

$$
\delta_{n} = \oint\vec{A}_{n}(\vec{R}) d \vec{R}\tag{3} 
$$
were $\vec{A}_{n}= i \braket{ \psi_{n} | \nabla_{R}\psi_{n} }$.
___
## Example: Uniform $\vec{B}$ field with spin 1/2 particles

We have $H(t) = \frac{e}{m} \vec{S} \cdot \vec{B}(t)$
where $\vec{B}(t) = B_{0}(\sin \alpha \cos \omega t, \sin \alpha, \sin \omega t, \cos \alpha)$ 
and $\vec{S} = \frac{\hbar}{2} \vec{\sigma}$
we have 
$$
H(t) = \hbar \frac{\omega_{1}}{2}\begin{pmatrix}
\cos \alpha & e^{-i \omega t \sin \alpha} \\
e^{i \omega t} \sin \alpha & -\cos \alpha
\end{pmatrix} \tag{4} 
$$
with intrinsic frequency  $\omega_{1} = \frac{eB_{0}}{m}$. The adiabatic condition is when $\omega_{1} \gg \omega$

if we diagonalize $(4)$ and eigen-decompose it, we will ge 
$$
\begin{align}
\chi_{+}(t) &= \begin{pmatrix}
coa \frac{\alpha}{2} \\
e^{i \omega t}\sin \frac{\alpha}{2}
\end{pmatrix} \ \ \ \ E_{+} = \frac{\hbar\omega_{1}}{2} \\
\chi_{-} (t) &= \begin{pmatrix}
e^{-i \omega t \sin \alpha/2} \\
-\cos \frac{\alpha}{2}
\end{pmatrix} \ \ \ \ E_{-} = -\frac{\hbar\omega_{1}}{2}
\end{align}
$$
Just solve the equation will grant us (check)
$$
\begin{align}
\chi(t) &=\left[ \cos \frac{\lambda t}{2} - i \omega_{1}-\frac{\omega \cos\alpha}{\lambda} \sin \frac{\lambda t}{2}  \right] e^{-i \omega t/2} \chi_{+}(t) \\
& +i \left[ \frac{\omega}{\lambda} \sin\alpha  \sin \frac{\lambda t}{2} \right] e^{ i \omega t/2} \lambda_{-}(t)
\end{align}
$$
where $\lambda = \sqrt{ \omega^{2} + \omega_{1}^{2} -2 \omega \omega_{1} \cos \alpha }$ .

Let us consider a transition from $\chi_{+}(0)\to \chi_{-}$ , we have the probability for such transition to be 
$$
P(t) = \lvert \braket{ \chi_{-}(t) | \chi(t) }  \rvert^{2} = \left( \frac{\omega}{\lambda} \sin \alpha  \sin \frac{\lambda t}{2} \right) ^{2}
$$
If we use the condition of adiabaticity $\omega_{1} \gg \omega_{0}$ , we have 
$$
\begin{align}
\lambda & \approx\omega_{1} - \omega \cos \alpha \\
P(t) &\approx \left( \frac{\omega}{\omega_{1}} \sin \alpha \sin \frac{\lambda t}{2} \right)^{2} \ll 1
\end{align}
$$
So there is a small (but none zero) chance that our state flip from $\lambda_{+}$
to $\lambda_{-}$

Now, what happens under a full rotation?

Using the condition for adiabaticity which gives us $\lambda \approx \omega_{1} - \omega \cos \alpha$ 
We can re-write $\chi(t)$ to be 
$$
\begin{align}
\chi(t) & \approx e^{-i \lambda t/2}e^{-i \omega t/2} \chi_{+}(t) \\
 & = e^{-i \omega_{1}t/2}e^{i \omega \cos (\alpha) t/2  } e^{- i \omega t / 2} \chi_{+}(t)
\end{align}
$$
We can then get from inspection that $\theta_{+}(t) = - \frac{\omega_{1}t}{2}$ and $\delta_{+}(t)= \frac{\omega t}{2}(\cos \alpha -1)$ 

We realize that $\delta_{+}(T)$ after one complete rotation is nothing but $-\frac{1}{2}\Omega$, the solid angle of the circle swept by $\vec{B}$ on the top of the sphere.

We discussed a situation where we have circular motion, but what if we have a general enclosed path?
We still have that  ($\alpha\to \phi, \beta\to \theta$)
$$
\chi_{+}=\begin{pmatrix}
\cos \frac{\theta}{2}  \\
e^{i \phi} \sin \frac{\theta}{2}
\end{pmatrix}
$$
We want to compute $A_{+}$ as defined in $(3)$, so we will need to calculate $\nabla_{B} \chi$ . Since we are in spherical coordinate, we have 
$$
\nabla_{B} \chi = \frac{1}{r} \begin{pmatrix}
\frac{1}{2} \sin \frac{\theta}{2}  \\
\frac{1}{2} e^{i \phi} \cos \frac{\theta}{2}
\end{pmatrix} \hat{\theta} + \frac{1}{r \sin \theta} \begin{pmatrix}
0 \\
i e^{i \phi} \sin \frac{\theta}{2}
\end{pmatrix} \hat{ \phi}
$$
This gives 
$$
\braket{ \chi_{+} |\nabla_{B} \chi_{+} } = \frac{i \sin^{2} \frac{\theta}{2}}{r \sin \theta} \hat{\phi} = \frac{i}{2} \frac{1}{r} \tan \frac{\theta}{2} \hat{\phi} \tag{5} 
$$
using $(3)$ gives:
$$
\delta_{n} = \oint \hat{A_{n}} \cdot d \vec{R}  = \int (\nabla_{R} \times A_{n}) \, d \vec{a} = \int \vec{B}_{n} \, d \vec{a} \tag{6} 
$$
we can see that $A_{n}$ actually becomes a fictitious magnetic field! This is called the `Berry field`

combine $(5)$ and $(3)$ gives
$$
\vec{A}_{=} = i \braket{ \chi_{+} | \nabla_{B} \chi_{+} }  = -\frac{1}{2r} \tan \frac{\theta}{2} \hat{\phi}
$$
This gives 
$$
\vec{B}_{+} = \nabla_{B} \times  \vec{A}_{+} = - \frac{1}{r \sin \theta} \frac{\partial}{\partial \theta} \left( \sin \theta  \frac{1}{2r}\tan \frac{\theta}{2} \right) \hat{r} = -\frac{1}{2r^{2}} \hat{r} \tag{7} 
$$
note that our $\vec{B}_{+}$ points radially! This is equivalent to a mono-pole magnetic charge at the origin! 

Because $d \vec{a} = \hat{r} r^{2} d\Omega$ , combine $(6)$ and $(7)$ gives 
$$
\delta_{+}(T) = \int  \vec{B} \cdot \, d \vec{a} = -\frac{1}{2} \Omega
$$
So  the result we got from a circular close contour is actually general to any close contour!