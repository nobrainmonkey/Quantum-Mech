From last time, we say the wave function after scattering could be written as 
$$
\Psi = \Psi^0 + GU\Psi \tag{1}
$$

which is an integral equation, and we chose:
$G^+ =\frac{e^{i \vec{k} \cdot r}}{r}\equiv$  $\Psi_{scatt}$ , and $\Psi_{0}=e^{i \vec{k} \cdot \vec{z}} \equiv J_{inc}$ 
Now, using Born's approximation, we have 
$$
\Psi= \Psi^0 + GU \Psi^0 + GUGU \Psi^0+ \dots \tag{2}
$$

Solving for the exact equation for $f(\theta,\phi)$ gives
$$
f(\theta,\phi)=\frac{m}{2\pi \hbar^2}\int e^{-i \vec{k} \cdot \vec{r}'} V(r') \Psi_{k}(r') \, d^3 r'  \tag{3}
$$

Combining $(2)$ and $(3)$ gives
$$
f_{Born}(\theta,\phi)=-\frac{m}{2\pi \hbar^2}\int e^{-i (\vec{k}_{f}-\vec{k}_{i}) \cdot \vec{r}'}V(r') \, d^3 r'  \tag{4}
$$
Note of equation $(4)$
1. The Born's approximation only use the first term of $(2)$ , which indicates $\Psi \approx \Psi^0$ . 
2. Note: The Born's approximation is valid when the potential term $V(r')$ is small compared to the initial kinetic energy $\frac{\hbar^2k_{i}^2}{2m}$.
3. $f_{Born} \sim \mathscr{F}(V(r'))$ 
4. $f_{born}$ depends on energy $E=\hbar \frac{k^2}{2m}$ , which relate with $\vec{q},|\vec{q}|$ 
5. $f_{born}$ depends on $\theta$ in the form of $e^{-i \vec{q} \cdot \vec{r}'}$
6. $f_{born}$ has do dependency on $\phi$ because our problem have cylindrical symmetry around $\hat{z}$ 

Note for wave vector $\vec{k}$ 
we have our initial wave vector $\vec{k}_{i}$ and final wave vector $\vec{k}_{f}$ , and the angle between them $\theta$, and we also have $|\vec{k}_{i}|=|\vec{k}_{f}|$ because the collision is elastic,
we then have 
$$
\vec{q} \equiv \vec{k}_{f} - \vec{k}_{i} = 2k\sin \frac{\theta}{2}
$$
Then we can re-write $(4)$ as 
$$
f_{Born}(\theta,\phi)=-\frac{m}{2\pi \hbar^2}\int e^{-i \vec{q} \cdot \vec{r}'}V(r') \, d^3 r'  \tag{5}
$$
We have Spherical Symmetry,so equation $(5)$ can be simplified 

$$
f_{born}(\theta)=\int e^{-i \vec{q} \cdot \vec{r}'} V(r') \, d^3 r'= \int_{0}^{\infty} \int_{0}^{\pi} \int_{0}^{2\pi} r'^2 \sin \theta e^{iqr' \cos \theta} \, d\phi  \, d\theta  \, dr' \tag{6}
$$

By just doing integration, we have 

$$
f_{born}(\theta)=\frac{2m}{\hbar^2}\int_{0}^{\infty} r' \frac{\sin(qr')}{q} V(r')\, dr' 
$$

_____________________________________________________________________________
Example 1: $V(r)=g \frac{e^{-\mu r}}{r}$
$$
f_{born}(\theta)=-\frac{2mg}{\hbar^2q}\int_{0}^{\infty} e^{-\mu r'}    \frac{e^{iqr}-e^{-iqr}}{2i} \, dr'  =-\frac{2mg}{\hbar^2(q^2+\mu^2)}
$$
$$
\sigma_{born}(\theta) = \frac{4m^2g^2}{\hbar^4\left[ 4k^2\sin^2 \frac{\theta}{2} +\mu^2 \right]^2}
$$
Note, when energy is large $\implies k =$ large, $\sigma_{born}(\theta)\to 0$ 
Be cautious that we can not take $\mu\to 0$, because if we do so, $V(r) \to \frac{1}{r}$ which is no longer "local", but let's do it anyway. This will yield us 
$$
\sigma_{born} (\theta) \  \text{"}=\text{"} \  \frac{g^2}{16E^2\sin^4 \frac{\theta}{2}}
$$
Now we want to know, when is this approximation valid?
1. We already discussed at high kinetic energy compared with $V(r)$
2. $|\Psi_{scatt}(r)| \ll |\Psi_{inc}(r)|$ , where $\Psi_{inc}(r)=e^{ik \cdot \vec{z}}$  $|\Psi_{scatt}| = \frac{m}{\hbar^2 k} | \int_{0}^{\infty} V(r')\sin(kr')e^{ikr'} \, dr'|$ 
where $\sin(kr')e^{ikr'}= \frac{e^{2ikr'}-1}{2i} \approx -\frac{1}{2i}$ $\implies \frac{m}{\hbar^2 k} |\int_{0}^{\infty} V(r) \, dr' | \ll 1 \implies \frac{m|V_{0}|r_{0}}{\hbar k} \ll 1$ . This gives$E = \hbar^2 \frac{k^2}{2m} \gg \frac{|V_{0}|^2}{\frac{\hbar^2}{mr_{0}^2}}$ 

Not gonna lie I don't quite get the physics intuition here beyond the fact that we must have $E\gg V_{0}$. I suppose we just require $r_{0}^2 |V_{0}|^2$ to be small now? 