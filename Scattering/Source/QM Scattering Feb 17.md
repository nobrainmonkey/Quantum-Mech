Recap: Scattering 
$\psi_{k}(\vec{r})\sim_{r\to \infty} A\left[ e^{ikz}+\frac{f(\theta,\phi)e^{ikr}}{r} \right]$ 
Where the first term is the incident wave, and the second term is the outgoing spherical wave
$\sigma(\theta,\phi) = | f(\theta,\phi)|^2$  where $f(\theta,\phi)$ is the scattering amplitude 
This lecture: find $f(\theta,\phi)$ give $V$ 


## Integral Equation
We have the integral equation formulation of Schrodinger's Equation 
$$
\psi_{k}(\vec{r})=\psi_{k}^0(\vec{r})+ \int G(\vec{r}-\vec{r}')U(r')\psi_{k}(r') \, d^3 \vec{r}' \tag{1}
$$
where $\psi_{k}^0$ is the free particle solution 
$$(\nabla^2 +k^2)\psi_{k}^0 =0 \tag{2}$$
and $G$ satisfy $$(\nabla^2 +k^2)G(\vec{r}-\vec{r}')=\delta(\vec{r}-\vec{r}') \tag{3}$$


Task #1: $\text{integral equation}\equiv \text{Schrodinger's equation}$ 
We prove $(\nabla^2 +k^2)$ acting on $(1)$ 
$$
(\nabla^2 +k^2)\psi_{k}=(\nabla^2 + k^2)\psi_{k}^0 + \int (\nabla^2 +k^2)G_{k}(\vec{r}-\vec{r}')U(r')\psi(r') \, d^3 \vec{r'} 
$$
Using $(2)$ and $(3)$, we have 
$$
\begin{align}
(\nabla^2 +k^2)\psi_{k}&=0 + \int \delta(\vec{r}-\vec{r}')U(r')\psi_{k}(r') \, d^3 \vec{r'} \\

(\nabla^2 + k^2)\psi_{k}  & =U(\vec{r})\psi_{k}(\vec{r})
 
\end{align}

$$
which is just the Schrodinger's equation 

Task #2:  Find $G_{k}(\vec{r}-\vec{r}')$ 
$$
(\nabla^2 +k^2)G_{k}(\vec{r})=\delta(\vec{r}) \tag{let $r'$=0}
$$
We will check that 
$$
G_{k}^{\pm} = -\frac{1}{4\pi} \frac{e^{\pm ikr}}{r} \tag{HW \#5}
$$
Note that we used $\nabla^2 G = \nabla\cdot \nabla G$ , and work this out in spherical polar coordinates.
Another tip: $\nabla^2 (\frac{1}{r}) =-4\pi \delta^{(3)}(r)$
and 
$G^+ \to \text{outgoing sph. wave} \checkmark$
$G^- \to \text{imploding sph. wave} \times$
Keep only $G^+$ in equation (1)
$$
\psi_{k}(\vec{r})=A\left[ e^{ikz}-\frac{1}{4\pi}\int \frac{e^{ik|\vec{r}-\vec{r}'|}}{|\vec{r}-\vec{r}'|} U(r') \psi_{k}(\vec{r}')\, d^3\vec{r}'  \right] \tag{4}
$$
Note that our Green's function has B.C. build in. Therefore, this is more convenient than Schrodinger's equation 

Note also $(4)$ is valid for all value of $r$ . 

Task 3: Let's use $(4)$ to see if we can retrieve large $r$ behavior and find $f(\theta,\phi)$ 
$$
\int d^3\vec{r}' \ \text{in equation } (4) \ \text{is restricted to } |\vec{r}'\leq R_{0}| 
$$
Look at $|\vec{r}'| \leq R_{0}\ll|\vec{r}|$ 
Under these conditions, 
$$
\begin{align}
|\vec{r}-\vec{r}'|&=(r^2+r'^2-2rr'\cos \alpha)^{1/2} \\
&=r\left[ 1+\left( \frac{r'}{r} \right)^2-2\left( \frac{r'}{r} \right)\cos \alpha \right]^{1/2}\\
&\approx r\left[ 1-\frac{r'}{r} \cos \alpha+O\left( \frac{r'}{r} \right)^2\right] \\
&\approx r-r'\cos \alpha+\dots\\
&\approx r-r' \cdot\hat{r}
\end{align}
$$

Plug into $(4)$ 
$$
\psi_{k}(\vec{r}) \approx_{r\to \infty}A\left[ e^{ikz}- \frac{1}{4\pi} \frac{e^{ik\vec{r}}}{r}\int e^{-ik \vec{r}' \cdot\hat{r}} U(r')\psi_{k}(\vec{r}') \, d^3 \vec{r}'  \right] \tag{5}
$$Note that we didn't make the approximation that $r-r' \approx r$ on the phase term because the maximum phase is $2\pi$ . Therefore, even though $r' \ll r$ , we can not ignore it in the phase term 
Note that the integral term in $(5)$ is simply $f(\theta,\phi)$
$$
\implies f(\theta,\phi)= -\frac{1}{4\pi}\int e^{-ik \vec{r}' \cdot\hat{r}} U(r')\psi_{k}(\vec{r}') \, d^3 \vec{r}' \tag{6}
$$
Note that $\psi_{k}(\vec{r}')$ is still in $(6)$ . Therefore, we are not done.


## Solving the Integral Equation
$$
\psi = \psi^0 +GU\psi
$$
Suppose $U\psi\ll K\psi^0$ where $K$ is the kinetic energy of the incident wave. And use the recursive approximation.
$$
\begin{align}
\psi &= \psi + GU(\psi^0+GU\psi) \\
&= \psi^0 + GU\psi^0 +(GUGU\psi^0+ + GUGUGU\psi^0\dots)
\end{align} \tag{7}
$$
Where if we use the first two terms on $(7)$ , the method is called "Born Approximation"

### Born Approximation 

$$
f(\theta,\phi)= -\frac{1}{4\pi} \int e^{ik\vec{r}'\cdot r} U(r') e^{ik\hat{z} \cdot \vec{r}'} \, d^3\vec{r}' \tag{8}
$$ where the third term in $(8)$ is $\psi^0_{k}(\vec{r}')$ with $\vec{k}=k \hat{z}$
Now we finally can compute $\sigma_{\text{Born}}(\theta,\phi)$ .
