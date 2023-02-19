## Helium Atom Cleanup
Hamiltonian:
$$
H=H_{1}+H_{2}+H_{12}
$$ 
We have our trial wave function 
$$
\Psi(\vec{r_{1}}\sigma_{1},\vec{r}_{2}\sigma_{2})=\Phi(\vec{r}_{1} \vec{r}_{2}) \frac{\ket{\uparrow \downarrow}-\ket{\downarrow\uparrow}}{\sqrt{ 2 }} 
$$
We said a natural choice for $\Phi(r_{1},r_{2}) = \psi_{100}(\vec{r}_{1}) \psi_{100}(\vec{r}_{2})=\frac{Z'^3}{\pi a_{0}^3}e^{-Z(r_{1}+r_{2})/a_{0}}$    
Where $Z'$ is a variational parameter.

check $\braket{ \Psi |\Psi  }=1$ 
$$
\begin{align}
\epsilon &= \bra{\Phi}(H_{1}+H_{2}+H_{12})\ket{\Phi} \\
&= \int \int \Phi^{*}(\vec{r}_{1},\vec{r}_{2}) \left[ \left( \frac{\hbar^2}{2m}(\nabla_{1}^2 -\nabla_{2}^2) \right) + \left( -\frac{2e^2}{r_{1}}-\frac{2e^2}{r_{2}} \right) +\left( \frac{e^2}{r_{12}} \right) \right] \Phi(\vec{r}_{1},\vec{r}_{2}) \, dr_{1}  \, dr_{2}
\end{align}
$$ How to do this intergal?
	*See Sakurai section 7.4*

It turns our the first two terms in the brakets are easy, while the last term is difficult. This is because for the first two terms, the two variables are completely seperable.

For the third term, we will need to use 
$$
\frac{1}{r_{12}}=\frac{1}{\sqrt{ r_{1}^2 +r_{2}^2 - 2r_{1}r_{2}\cos \gamma}}= \sum_{l=0}^\infty \frac{r_{<}^l}{r_{>}^{l+1}}P_{l}(\cos \gamma)
$$ Just do the integral, and we should have the answer 
$$
\epsilon=\left(\frac{e^2}{a_{0}}\right)\left[ 2\cdot \frac{Z'^2}{2}-2\cdot 2Z' +\frac{5}{8}Z'\right] 
$$ Optimal value of $Z'^{*}$ is given by 
$$
\frac{\partial\epsilon}{\partial Z'^{*}} =0 \implies Z'^{*} = 2-\frac{5}{16}
$$
Note that our optimal $Z' <2$. This is physical because one of th electron "sheilds" the other electron from nucleus.

Best variational estimate of the gound state energy of the helium atom 
$$
\epsilon(Z'^{*}) \approx -77.5 \text{eV}
$$
The experimental value (double ionization)
$$
E_{0} = -78.6 \text{eV}
$$
Note that $\epsilon(Z') \geq E_{0}$. This is a constraints for variational method.



## Scattering 

### Assumptions:
1. We assumes collisions are none-relativistic
2. Elatistic Scattering
3. No new particle created

The geometry of the scattering: 
* Cast I
![[Scattering Cast 1.png]]
* Case 2
![[Scattering Cast 2.png]]
With the assumptions above, case 2 can be reduced to case 1.

Cast 2:
$$
H = -\frac{\hbar^2}{2m_{1}}\nabla_{1}^2-\frac{\hbar^2}{2m_{2}}\nabla_{2}^2 + V(\vec{r}_{1}-\vec{r}_{2}) \tag{Lab Frame}
$$ We can change this to center of mass coordiate 
$$
\begin{align}
\vec{R}  & = \frac{m_{1}\vec{r}_{1}+m_{2}\vec{r}_{2}}{m_{1}+m_{2}} \\
\vec{r} & = \vec{r}_{1}-\vec{r}_{2} \\ \\
M  & =m_{1}+m_{2} \\
m  & = \frac{m_{1}m_{2}}{m_{1}+m_{2}}
\end{align}
$$
This gives 
$$

H = -\frac{\hbar^2}{2M}\nabla_{R}^2-\frac{\hbar^2}{2m}\nabla_{r}^2+V(\vec{r}) \tag{CoM frame}
$$
where 
$$
\Psi(\vec{r}_{1},\vec{r}_{2})= \Phi_{cm}(\vec{R})\psi(\vec{r})
$$
Because we can always use this transformation, we can focus on case one.

## Scattering crosssestion 
![[Scattering Cross Section.png]]
The incident Flux $\vec{J}_{inc}=J_{inc}\hat{z}$ , $J=\text{number of particle per unit area per unit time }$ 
The dector distance $r$ away measures # of particles scattered into the detector per unit time 
measurement $= J_{inc} \sigma(\theta,\phi) d\Omega$  where $\sigma(\theta,\phi)$ is the definition of the scattering cross section.
Note: some book call $\sigma(\theta,\phi) \leftrightarrow \frac{d\sigma(\theta,\phi)}{d\Omega}$ . It is crucial to realize $[\sigma(\theta,\phi)]=L^2$ 

Scattering flux into detector $J_{scatt}=\frac{\text{\#of particle per unit time }}{\text{Area of detector}} = \frac{J_{inc}\sigma(\theta,\phi)}{r^2 d\Omega}$ 
$\implies \sigma(\sigma,\phi) = \frac{r^2J_{scatt}}{J_{inc}}$ 
