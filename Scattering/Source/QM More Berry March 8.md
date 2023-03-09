## Recap:
We realize that when the change in Hamiltonian $H$ over time $\dot{H}$ is small when compared with the equivalent time energy difference between instantaneous eigenstates $E_{n} - E_{m}$ , which means $\left\lvert  \sum_{n \neq m} \frac{\bra{\psi_{m} }\dot{H}\ket{\psi_{n}}}{E_{n}-E_{m}}  \right\rvert \ll 1$ , we can use the adiabatic approximation. We obtain our final coefficient relation that 
$$
\dot{c}_{m}(t) = -c_{m}(t) \bra{\psi_{m}} {\ket{\dot{\psi}_{m}} }  \tag{1}
$$

___
## Geometric phase:
The solution for $(1)$ is that 
$$
c_{m}(t) = c_{m}(0)e^{i \delta_{m}(t)} \tag{2} 
$$

where we obtain `geometric phase`
$$
		\delta_{m}(t) = i \int_{0}^{t} \bra{\psi_{m}(t')} \frac{\partial}{\partial t}\ket{\psi_{m}(t')}  \, dt' \tag{3} 
$$

so that we can write our wave function with the coefficient values in $(2)$ and get 
$$
\Psi(t) = \sum_{n} c_{m}(0) \psi_{n}(t)e^{i \theta_{n}(t)}e^{i \delta_{m}(t)} \tag{4} 
$$

If we have the special case where 
$$
\begin{align}
c_{n}(0)  & =1 \\
c_{m}(0) & = 0 \forall m \neq n
\end{align}
$$

We then get the case where the total wave function $(4)$ gets reduced to a stationary state $\psi_{n}$ with the dynamic phase and the geometric phase:
$$
\Psi(t) = \psi_{n}(t) e^{i \theta_{n}(t)}e^{i \delta_{n}(t)} \tag{5} 
$$

We note that $\delta_{m}$ is real, because 
$$
\begin{align}
\braket{ \psi_{m}(t) | \psi_{m}(t) }  & =1 \\
\frac{\partial}{\partial t} \braket{ \psi_{m}(t) | \psi_{m}(t) }  & =0 \\
\braket{ \dot{\psi}_{m} | \psi_{m} } + \braket{ \dot{\psi}_{m} | \psi_{m} }  & =0 \\
2 \text{Re} \braket{ \psi_{m} | \dot{\psi}_{m} }  & =0
\end{align}
$$

and combine the $i$ in front of $(3)$ gives that $\delta_{m} \in \mathbb{R}$.

___
## Closed Contour 

If $\psi$ has $\vec{R}(t)$ dependence, we can write that 
$$
\frac{\partial}{\partial t} \psi_{m}(\vec{R}(t)) = \frac{\partial \psi_{m}}{\partial R_{1}}\frac{\partial R_{1}}{\partial t}  + \frac{\partial \psi_{m}}{\partial R_{2}}\frac{\partial R_{2}}{\partial t} + \frac{\partial \psi_{m}}{\partial R_{3}}\frac{\partial R_{3}}{\partial t}  
= \nabla_{R} \psi_{m} \cdot \frac{\vec{\partial}R}{\partial t} 
$$

Using this formulation with $(3)$ will result in 
$$
\delta_{n}(t) = i \int_{0}^{t} \braket{ \psi_{m} | \dot{\psi}_{m} }  \, dt' = i\int_{0}^{t} \braket{ \psi_{n} | \nabla_{R} \psi_{m} } \frac{d\vec{R}}{dt}  \, dt := \int_{R_{i}}^{R_{f}} \vec{A}_{n}(\vec{R}) \, d\vec{R}   
$$

However, "phases" are not real physical observable. Therefore, we consider the gauge dependence of $\delta_{n}(t)$ so that:
$$
\psi_{n}(\vec{R}(t)) \to \psi_{n}'(\vec{R}(t)) = \psi_{n}(\vec{R}(t)) e^{i \zeta_{n}(\vec{R}(t))} \tag{6} 
$$

This gauge transformation gives:
$$
\begin{align}
\vec{A}_{n} & \to \vec{A}_{n}' = \vec{A}_{n} - \nabla_{R}\zeta_{n}(\vec{R})  \\  \\
\delta_{n}(t)  & \to \delta_{n}'(t) = \delta_{n}(t)-\zeta(\vec{R}_{f})+ \zeta(\vec{R}_{i})
\end{align}
$$

and we if have a closed contour, we have $\vec{R_{i}}=\vec{R}_{f}$, and therefore 
$$
e^{i \zeta_{n}(\vec{R}_{i})}=
e^{i \zeta_{n}(\vec{R}_{f})}
$$

Therefore, we must have that 
$$
\zeta_{n}(\vec{R}_{f})- \zeta_{n}(\vec{R}_{i}) = 2 \pi n \ \text{for} \ n \in \mathbb{Z}
$$

Therefore, for a closed contour, $\delta_{n}(t)$ is actually a physical phase as a gauge transformation **cannot** cancel $\delta_{n}(t)$. Therefore, $\delta_{n}(t)$ is physical.
___
## A classical example:
![[Pasted image 20230308120803.png]]
Note that any rotator starting from $1$ , and go through a closed contour as the diagram indicated, we realize the plane of the rotation changes.
This process is called a `Non-holonomic transport`, or `paralled transformation` in differential geometry.
On the example above, I claim that the shift in the plane of rotation $\theta = \Omega$, the solid angle of the surface. This is because 
$$
A = \frac{2\pi R^{2}}{2 \pi / \theta}\to \theta=\frac{A}{R^{2}} = \Omega
$$

This happens because the surface of a  sphere has intrinsic curvature (not homeomorphic to $\mathbb{R}^{2}$).
___
## Measurement of Berry Phase
We know our wave function have a total phase (dynamic + Berry)

$$
\Psi_{n}(t) = \psi_{n}(t) e^{i \theta_{n}(t)} e^{i \delta_{n}(t)}
$$

and Berry phase is nothing but a $T$ period angle change of $\vec{R}(t)$ , so $\delta_{n}(T) =$ Berry phase. But note that after $T$, our dynamic phase becomes $1$. Therefore 
$$
\Psi = \psi_{0} + e^{i \delta_{n}} \to \lvert \Psi \rvert ^{2} = \lvert \psi_{0} \rvert ^{2}(1+\cos \delta_{n})
$$

___
## Example: Spin in a rotating magnetic field.

Let's consider we have a rotating spin $\frac{1}{2}$ particle under a uniform magnetic field. If we express the strength of $\vec{B}$ over time, we have: 
$$
\vec{B} =B_{0} (\sin \alpha \cos(\omega t),\sin \alpha \sin(\omega  t), \cos \alpha)
$$

in polar coordinates with angle $\alpha$ and our spin $\frac{1}{2}$ particle is rotating with a frequency $\omega$ in the uniform magnetic field, with our Hamiltonian 
$$
H(t) = \frac{e}{m} \vec{S} \cdot \vec{B}
$$

and $\omega_{1} = \frac{eB_{0}}{m}$ which is called the cyclotron frequency. Note that the adiabatic condition is when $\omega_{1} \gg \omega$.

Just diagonalize $H(t)$ gives our instantaneous eigenstates 
$$
\begin{align}
\chi_{+}(t)  & = \begin{pmatrix}
\cos \frac{\alpha}{2}  \\
e^{i \omega t \sin \alpha/2}
\end{pmatrix} \ \ \ \ E_{+} =  \frac{\hbar\omega_{1}}{2}
 \\
 \\
\chi_{-}(t)  & = \begin{pmatrix}
e^{-i \omega t}\sin \frac{\alpha}{2}  \\
-\cos \frac{\alpha}{2}
\end{pmatrix} \ \ \ \ E_{-} =  \frac{-\hbar\omega_{1}}{2}
\end{align}
$$