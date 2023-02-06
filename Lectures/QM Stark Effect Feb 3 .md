# QM Stark Effect Feb 3

## Stark Effect
$H_0$: H-atom

$H_1=e E r\cos{\theta}$

$H_1 \doteq \begin{pmatrix}
    0& \Delta & 0 & 0 \\
    \Delta & 0 & 0 & 0 \\
    0 & 0& 0 & 0   \\
    0 & 0& 0 & 0
\end{pmatrix}$

Note that $\bra{nlm} H_1 \ket{n'l'm'} \neq 0 \iff m=m', l=l\pm 1$ 

The proof of the above state uses the fact that :

$Y_0 ^0 \approx 1, Y_1^{\pm 1} \approx \sin\theta e^{\pm i \phi}, \text{and} Y_1^0 \approx \cos \theta$

Due to this selection rule, the only non-zero elements are 

$\bra{210} H_1 \ket{200} = \bra{200} H_1 \ket{210}^* = \Delta$

(do integral to very this): $\Delta =-3 e E a_0$

Next step: FInd the Eigensystem of the matrix

Eigenvalue: $\pm \Delta , 0 ,0$, Eigenvector:$\frac{1}{\sqrt{2}}(\ket{200} \pm \ket{210}), \ket{211}, \ket{21-1}$


for $n=2$ state, our result tells us the degenerate energy level splits into 3 energy levels $E^0_2 + 3ea_0 E, E^0_2, \text{and} E^0_2 -3ea_0 E$ 

### Corollary to the Stark Effect
This is imporant because it shows that perterbation _may_ break degenercy depending on the problem's setup. This is because many times perterbation might change/break the symmertry of the system.

Note that if the state has not definite parity, we then __cannot__ use the parity arguement to elimate first order perterbation. This gives our $n=2$ states linear perterbation term. Note that this is __different__ from $n=0$ state.


## Fine Structure of Hydrogen Spectrum
$H_0 = \frac{p^2}{2m} - \frac{e^2}{r}$

The velocity of the lectron (e.g. 1s state) $mv^2 \approx \frac{me^4}{\hbar ^2} \Rightarrow \frac{v}{c} \approx \frac{e^2}{\hbar c}\approx \frac{1}{137} << 1$. Therefore, the velocity of the electron is small compared to the speed of light, so we can use perterbation theory:

* Write down Dirac theory of relativistic electron
* epxpand in $\frac{v}{c} <<1$
  
We then get $H = mc^2 +\frac{p^2}{2m}-\frac{e^2}{r}+ H_\textrm{relativistic}$

Where the first 3 terms are the non-relativistic hydrogen ateom hamiltonian $\approx 10 \textrm{eV}$, and 
$R_y = \frac{1}{2}\frac{me^4}{\hbar^2} = \frac{1}{2}(\frac{e^2}{\hbar c})^2 mc^2 = \frac{1}{2} \alpha^2 mc^2$

Note that $H_\textrm{relativistic}\propto O(\alpha^4 mc^2)$ and 

$H_\textrm{relativistic} = - \frac{p^4}{8m^3c^2}+ \frac{e^2}{2m^2c^2}\frac{1}{r^3} \hat{L} \cdot \hat{S} + \frac{\pi e^2 \hbar^2}{2m^2 c^2} \delta(r)$  
$H_\text{relativistic}= H_K + H_{SO}+ H_{D}$

1. $H_K$ come from expanding 
    
    * $E = \sqrt{p^2 c^2 +m^2 c^4}=mc^2\sqrt{1+\frac{p^2}{m^2c^2}} \approx mc^2 + \frac{p^2}{2m}- \frac{p^4}{8m^3c^2}$.

    * It's magnitude $\frac{H_k}{H_0} \approx \frac{\frac{p^4}{8m^3 c^2}}{\frac{p^2}{2m}} \approx \alpha^2$

2. $H_D$ 

    * Compton wavelength $\approx \frac{\hbar}{mc}$
    
    * This means interaction becomes none local at this order of magnitude

    * $V(r)\rightarrow \int {\text{d}}^3 \rho f(|{\rho}|)$
    $\int \text{d}^3 f(|\rho|)=1$ and $f=0$ for $|\rho|\leq \frac{\hbar}{mc}$
    We then taylor expand $V(r)$

      * $\delta(\vec{r}) \rightarrow$ only $l=0$ state is affected by $H_D$  

    * Order of magnitude of $H_D$
    
       * $H_D \approx \frac{e^2 \hbar^2}{m^2 c^2 |\psi(0)^2|}$, and $\frac{H_D}{H_0} \approx \alpha ^2$




