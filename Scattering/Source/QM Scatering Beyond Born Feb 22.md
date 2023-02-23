## Recap
The motivation of going beyond the Born's approximation is  the following:
* Can not work for low potential energies
* For some potentials, the Fourier Transform does not exist 
Note that to address the low potential case, we can simply use Perturbation Theory, So let us discuss the mathematics on point 2.

We have the exact answer 
$$
\Psi = \Psi^0 + GU\Psi \approx_{\text{born}} \Psi^0 +GU\Psi^0 \tag{1}
$$
Note that the exact solution of $\Psi$ must equal to zero when $U$ diverges. However, in $\text{(1)}$ , we approximated it with a plane wave $\Psi^0$ . This is why we cannot do a Fourier Transformation when $U$ diverges.
____
## Partial Waves/Phase Shifts
### Incident Wave Expansion 
For a spherically symmetric potential $V(r)$, we can expand all quantities in angular momentum eigenstates.
First, we can write down the incident wave in angular momentum eigenstates
$$
\begin{align}
\Psi_{0} & =e^{ikz} \\
&=e^{ikr\cos(\theta)} \\
&= \sum_{l=0}^{\infty}i^l(2l+1)j_{l}(kr)P_{l}(\cos \theta)
\end{align} \tag{2}
$$

where $j_{l}$ is the spherical Bessel function and $P_{l}$ are Legendre Polynomials  
This is useful because any function $F(\theta,\phi)$ on the surface of the sphere can be expanded to $Y_{l}^m(\theta,\phi)$ , but if $F(\theta,\phi)$ is $\phi-$independent, this implies 
$$
Y_{l}^m(\theta)=Y_{l}^0(\theta)=\frac{2l+1}{4\pi}P_{l}(\cos \theta)
$$
Therefore
$$
\begin{align}
e^{ikr\cos \theta}= \sum_{l=0}^{\infty} c_{l}(kr)P_{l}(\cos \theta) \tag{3}
\end{align}
$$
Where, using Fourier coefficient expansion, and the orthogonality of Legendre polynomials,
$$
c_{l}(kr)= \frac{2l+1}{2}\int_{-1}^{1} e^{ikru}P_{l}(u) \, du \tag{4}
$$
where doing the integral in $(4)$ will finish the expansion of $(3)$

### Smarmy of Spherical Bessel Functions
$$
\begin{align}
j_{0}(x) & =\sin \frac{x}{x} \\
j_{1}(x) & =\frac{\sin x}{x^2}-\frac{\cos x}{x} \\
j_{2}{x}  & =  \left( \frac{3}{x^2} -\frac{1}{x}\right)\sin x-\frac{3}{x^2}\cos(x)\\
& \vdots \\
j_{l}(x) & =\left( \frac{\pi}{2x} \right)^{1/2} J_{l+\frac{1}{2}}(x)
\end{align}
$$
and let's analyze the limiting behavior of $j_{l}(x)$
For $x\ll 1$:
$$
\begin{align}
j_{l}(x)\approx \frac{x^l}{(2l+1)!!} \ \text{where} (2l+1)!! =(2l+1)(2l-1)\dots 5\cdot3\cdot1
\end{align}
$$
and for $x\to \infty$
$$
j_{l}(x)\sim \frac{1}{x}\sin\left( x-\frac{l\pi}{2} \right)
$$

Note that because $j_{l}$ is a solution to a **second order** ode. This means there must be another set of solution that satisfy our ODE. The other set of solutions is call the `Neumann Functions` Here are the first several Neumann functions:

$$
\begin{align}
n_{0}(x) & =-\frac{\cos x}{x} \\
n_{1}(x) & =-\frac{\cos x}{x^2}-\frac{\sin x}{x}
\end{align}
$$
When $x\to 0$
$$
n_{l}(x)\approx \infty 
$$
And when $x\to \infty$ 
$$
n_l{x}= (-1)^{l+1} \left( \frac{\pi}{2x} \right)^{1/2} J_{-l+\frac{1}{2}}(x)
$$
Note that the Neumann function is not particularly useful for our case. This is because at $r=0$ , $\frac{n_{l}(r)}{r}\to \infty$.
____
### Solving the Equation

We want to expand the solution of 
$$
\left[ -\frac{\hbar^2}{2m} \nabla^2 +V(r)\right] \Psi(r)=\frac{\hbar^2k^2}{2m} \Psi_{k}(r) \tag{5}
$$
in spherical harmonics; only $m=0$ as the incident plane wave only have component of $m=0$:
$$
\Psi_{k}=\sum_{l=0}^\infty \frac{u_{k,l}(r)}{r} P_{l}(\cos \theta) \tag{6}
$$
substitute $(6)$ into $(5)$ and get:
$$
\left[ -\frac{\hbar^2}{2m} \frac{d^2}{dr^2}+\frac{l(l+1)\hbar^2}{2mr^2} + V(r) \right]u_{k,l}(r)=\frac{\hbar^2k^2}{2m}u_{k,l}(r) \tag{7}
$$
We then want to solve for this equation for $r>0$ with $u_{k,r}(r=0)=0$ 
We first look at $r\to \infty$ solution, note that the centrifugal term will vanish, and we assume $V(r)$ is of a finite range, so we have :
$$
\left( \frac{d^2u}{dr^2} +k^2\right)u\approx_{0} \tag{8}
$$
This will give us two solutions $u \sim e^{\pm ikr}$ . We are tempted to only keep the outgoing wave solution, but now because our incoming wave is written in linear expansions, so we need to keep both solutions, so we have 
$$
u(r)\approx_{r\to \infty} A_{l}\sin\left( kr-\frac{l\pi}{2}+\delta_{l} \right) \tag{9}
$$
The reason we wrote our phase like this is so we can explicitly write out the phase that is different from $j_{l}$ as $x\to \infty$.  It turns out $\delta_{l}$ along with $k$ gives us the entire solution to the scattering cross section.