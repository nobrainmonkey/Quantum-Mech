## Variational Principle 
$$
E_{\phi}=\frac{\bra{\phi}H\ket{\phi}}{\braket{ \phi | \phi } }
$$
### Example 1
$$
H = \frac{p^2}{2m}+V(x)
$$
let $V(x)$ to be infinite square well situated at $x=a,x=-a$
We find a trial $\phi(x)$.  Our trial function is better if it satisfy:
1. Symmetric
2. No nodes
3. Vanished at $x=\pm a$
Try using trial function
$\phi(x)=N(x-a)(x+a)$ for $x \leq a$ , $\phi(x)=0$ for $x>a$ 
$\braket{ \phi | \phi }=\int \mid \phi(x)\mid^2 \, dx =1 \implies \text{fixes} \  N$ 
$\bra{ \phi}H\ket{\phi}=\int \frac{\hbar^2}{2m} |\frac{d\phi}{dx}|^2 + V(x) \mid \phi(x)\mid^2 \, dx$ 
Compute $E_{\phi}=\frac{\alpha \hbar^2}{ma^2}$ (find $\alpha$) 
Find the exact $E_{0}=\alpha_{0} \frac{\hbar^2}{ma^2}$

### Example 2: Helium Atom
$$
H=-\frac{\hbar^2}{2m}\Delta_{1}-\frac{2e^2}{r_{1}}-\frac{\hbar^2}{2m}\Delta_{2}-\frac{2e^2}{r_{2}}+\frac{e^2}{r_{12}}
$$
#### A digression on spin, statistics and symmetrization of identical particles in QM
In $d=3$ space $+1$ time dimension, all identical particles come in two types:

|Fermions | Bosons|
|----------------|-------------|
|Half integer spins  | integer spins|
| Electrons ...| Photons, Gluons...|
|Fermi-Dirac Statistics| Bose_Einstein Statistics|
|Symmetric under exchange| Anti-Symmetric under exchange|
Note:
$\vec{R_{i}}=(r_{i}m_{s_{i}})$ where $r_{i}$ is position, $m_{s_{i}}$ is the spin quantum number $S_{z}$ if needed
Any wave function for $N$ identical bosons:
$$\Psi_{B}(\vec{R_{1}}\vec{R_{2}}\dots\vec{R_{i}}\dots\vec{R_{j}}\dots\vec{R_{N}})=\Psi_{B}(\vec{R_{1}}\vec{R_{2}}\dots\vec{R_{j}}\dots\vec{R_{i}}\dots\vec{R_{N}})$$
Which is __Symmetric__ under particle exchange.
Any wave function for N identical fermions:
$$
\Psi_{B}(\vec{R_{1}}\vec{R_{2}}\dots\vec{R_{i}}\dots\vec{R_{j}}\dots\vec{R_{N}})=-\Psi_{B}(\vec{R_{1}}\vec{R_{2}}\dots\vec{R_{j}}\dots\vec{R_{i}}\dots\vec{R_{N}})
$$
Which is __Anti-Symmetric__ under particle exchange, and this anti-symmetry causes the __Pauli exclusion principle__.

Back to our Helium Problem 
$$
H=H_{1}+H_{2}+H_{12}
$$
As a first step ignore $H_{12}$
We can try using Hydrogen ground state wave function 
$\psi_{100}(\vec{r_{1}})\psi_{100}(\vec{r_{2}})$. However, this breaks our symmetry. So we have to change our spin state in combination with our wave function 

$$
\Psi =\psi_{100}(\vec{r_{1}})\psi_{100}(\vec{r_{2}}) (\frac{\ket{\uparrow \downarrow} - \ket{\downarrow \uparrow}}{\sqrt{ 2 }}) 
$$
where 
$$
\psi_{100}(\vec{r})=\left( \frac{Z^3}{\pi a_{0}^3} \right)^{1/2} e^{-Zr/a_{0}}
$$
This implies 
$$
\Psi(\vec{r_{1}}\vec{r_{2}})=\frac{Z^3}{\pi a_{0}^3}e^{-Z(r_{1}+r_{2})/a_{0}}
$$
Using Variational Method 
$$
\bra{\Psi} (H_{1}+H_{2})\ket{\Psi} =2 \left( -\frac{m(Ze^2)^2}{2\hbar^2} \right) \approx-108.8 \text{eV}
$$
Where the measured data is $E=-78.6\text{eV}$
* Note our variational method is __not__ larger because we didn't account for $H_{12}$.
* Note, we can introduce a variational parameter. The variation parameter we can change is $Z$. This is because an electron will create a partial shielding for the other electron.

