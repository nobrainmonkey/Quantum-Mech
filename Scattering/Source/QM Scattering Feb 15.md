We have an incident flux at $\hat{z}$ direction (plane wave) with a spherically symmetric potential.

Now, the plane wave is going to be scattered. We can put a detector at distance $r$ away with$d \Omega=d\phi d\theta \sin \theta$ (solid angle) 

And the scattering cross-section  
$$
\sigma(\theta,\phi)=\frac{r^2J_{\text{scatt}}}{J_{\text{inc}}}
$$
Given $V(r) \implies$compute $\sigma(\theta, \phi)$ as a function of energy.

----------------------------------------------
## 1-D Scenario 
We have a wave traveling to the right $Ae^{ikx}$ 
After scattering, there will be a reflected wave $R e^{-ikx}$ 
and a translated wave $Te^{ikx}$ 
We then use Schrödinger Equation to solve for $\frac{T}{R}$
The Asymptotic behavior is given.
______________________________________________
## 3-D Scenario
### Physics intuition <sup>TM</sup>`
the wave traveling in every direction, so we first find the asymptotic behavior, then solve the Schrödinger equation. 
The Asymptotic at $r\to \infty$ form of the wave function is 

$$ \psi \to A \left( e^{ikz}+f(\theta,\phi) \frac{e^{ikr}}{r} \right)$$
Where the first term described the incoming wave front toward $\hat{z}$ direction, and the second term describes a radially outward wave. The $\frac{1}{r}$ is due to probability conservation.
### Math Derivation 
#### Incident
$\psi_{\text{inc}}(r)=Ae^{\vec{k}\cdot\vec{r}}=Ae^{ikz}, E=\frac{\hbar^2k^2}{2m}$  
#### Scattering
$$\begin{align}
k^2 &= \frac{2mE}{\hbar^2},k>0 \\
U(r)&=\frac{2m}{\hbar}V(r)
\end{align}$$
By Schrödinger Equation 
$$
\Delta \psi+(k^2 -U(r))\psi=0
$$
Where $\Delta$ is the spherical polar coordinate
By separation of variable 
$$
\psi(\vec{r}) = \sum_{l,m} c_{l,m} Y_{l}^m(\theta,\phi) \frac{u_{l}(r)}{r}
$$
Therefore,
$$
\frac{d^2u}{dr^2}+\left[ k^2-U(r)-\frac{l(l+1)}{r^2} \right] u_{l}(r)=0
$$
Asymptotic behavior $r \to \infty \implies \frac{l(l+1)}{r} \to 0, U(r)\to{0} \forall U(r)$ decaying faster than $\frac{1}{r}$
Thus, we have  
$$
u_{l}'' + k^2u_{l}=0
$$
with the solution
$$
\begin{align}
\frac{u_{l}}{r} &\sim \frac{e^{ikr}}{r} \\
& \sim \frac{e^{-ikr}}{r} 
\end{align}
$$
However, we ignore the second solution as the wave function can only be "scattered out".
Therefore,
$$
\psi_{\text{scatt}}(r) \sim \sum_{l,m} c_{l,m} Y_{l}^m(\theta,\phi) \frac{e^{ikr}}{r} \sim f(\theta,\phi) \frac{e^{ikr}}{r}
$$
We will prove $\sigma(\theta,\phi) = \mid f(\theta,\phi)\mid ^2$. The name of $f(\theta,\phi)$ is "scattering amplitude".
### Probability Current
In QM.  Fluxes are probability current densities.
$$
\vec{J}=\frac{\hbar}{m} \mathrm{Im}(\psi^* \vec{\nabla}\psi )
$$
$\psi_{\text{inc}}= Ae^{ikz} \implies \vec{J_{\text{inc}}}=|A|^2 \hbar \frac{k}{m} \hat{z}$  
$\psi_{\text{scat}} \sim f(\theta,\phi) \frac{e^{ikr}}{r}= \vec{J_{\text{scatt}}}$
$$
\vec{\nabla}\psi= \frac{ \partial \psi }{ \partial r } \hat{r} + \frac{1}{r} \frac{ \partial \psi }{ \partial \theta } \hat{\theta}+\frac{1}{r \sin \theta} \frac{ \partial \psi }{ \partial \phi } \hat{\phi}$$
check that $\hat{\theta},\hat{\phi}$ component of $\vec{J}_{\text{scatt}}$ are negligible when $r\to \infty$ 
Compute $\vec{J}_{\text{scatt}}$ and show that 
$$
\vec{J}_{\text{scatt}}\approx|A|^2 \frac{\hbar k}{m} \frac{|f(\theta,\phi)|^2}{r^2}
$$
Therefore,
$$
\begin{align}
\sigma(\theta,\phi) & =r^2 \frac{|\vec{J}_{\text{scatt}}|^2}{|\vec{J}_{\text{scatt}}|^2}
\end{align}
$$
and check that 
$$
\sigma(\theta,\phi)=|f(\theta,\phi)|^2
$$
### Using Green's function so solve SE
Need to solve
$$
(\vec{\nabla^2}+k^2)\psi_{k}(\vec{r})=U(r)\psi_{k}(\vec{r}) \tag{*}
$$
with suitable B.C. 
Claim: It is easier to solve this problem by re-writing it as an integral equation.

$$
\psi_{k}(\vec{r})=\psi_{k}^0(\vec{r})+ \int G_{k}(\vec{r}-\vec{r}')U(r')\psi_{k}(\vec{r}) \, d^3\vec{r} \tag{**}
$$ where $\psi_{k}^0$ is the solution for homogeneous PDE, and $G$ is a Green's function satisfying 
$$
(\nabla^2+k^2)G_{k}(\vec{r}-\vec{r}') = \delta(\vec{r}-\vec{r}')
$$

