# QM Fine Structure of H Feb 6
We have Fine structure constant $\dfrac{e^2}{\hbar c} \approx \dfrac{1}{127} <<1$ 

We have the followting terms in our Hamiltonian 
$H = mc^2$ ~$10^6 eV$ 
	$+ \frac{p^2}{2m}-\frac{e^2}{r}$~$10eV$ 
	$+ H_k+ H_D +H_{soc}$~ $\alpha^2 mc^2 10^{-2}$eV
	$+...$ higher order in $\alpha$ 


## Spin Orbit Coupling(SOC) term 
$H_{soc} = \frac{1}{2} \frac{e^2}{m^2 c^2} \frac{1}{r^3} \vec{L} \cdot \vec{S}$ 
__where does this come from?__
### Derivation
Consider an $e^-$ of charge $-e$ in motion around a nucleus of $+Ze$ 
__In addition__ to Columb interaction,  a subtile relativitive effect $\rightarrow$ SOC.
In the rest frame of the $e^-$ , the moving nucleus leads to a $B$ field.
$\vec{B} = -\frac{1}{c} \vec{v}  * \vec{E}$ 
This leands to a Zeeman interaction 
$H_{soc} = - \vec{\mu} \cdot \vec{B}$  whtere $\vec{\mu}$ is the magnetic moment of the $e^-$ , and $\vec{\mu} = -g \mu_B \vec{S}/\hbar$ where $g$~$2$ , $\mu_B = \frac{e \hbar}{mc}, \vec{S}= \frac{1}{2}$ 
$\vec{E} = - \Lambda \phi = \frac{\vec{r}}{r} \frac{d \phi}{d r}$      
$\Rightarrow H_{soc} = -\frac{e}{mc^2}\vec{S} \cdot (\vec{v} \times \vec{r}) \frac{1}{r} \frac{d \phi}{d r}$ , $\phi(r) = -\frac{Z e}{r} \rightarrow \frac{d \phi}{ d r} = \frac{Z e}{r^2}$ . Also we have $\vec{L}= \vec{r} \times m \vec{v}$ 
$\Rightarrow H_{soc} = (\frac{1}{2}) \frac{Ze^2}{m^2 c^2} \frac{1}{r^3} \vec{L} \cdot \vec{S}$ 
Note that the $\frac{1}{2}$ comes from the none-intertial frame of the electron.


### Scaling  of SOC with $Z$ 
$\frac{\hbar ^2}{ma^2} \approx \frac{Z e^2}{a^2} \Rightarrow a \approx \frac{1}{Z}a_0$ 
$\langle \frac{1}{r^3} \rangle \approx \frac{1}{a^3}\approx \frac{z^3}{a_0^3}$. Therefore, $H_{soc} \propto Z^4$ 
Note that this scaling is a crude approximation of only one electron. Nevertheless, $H_{soc}$
increases rapidly with $Z$ 
for Hydrogen atom 
$L \approx \hbar$ , $S \approx \hbar$. Therefore, $H_{soc} \approx \frac{e^2}{m^2c^2} \frac{\hbar ^3}{a_0^3} \approx \alpha^4 mc^2$ . Check $\frac{H_{soc}}{H_0} \approx \alpha^2$ 

### (Detail in HW#4)Sketch of Fine Structure Peterb.
$n=1 , l=0, H_{soc}=0$ , we then start looking at $n=2$ level.
$H_k = \frac{-p^4}{8m^3c^2}$ term is rotational invariant as $p^4 = (p \cdot p)^2$ 
This means $H_k$ is already diagonal in the eigenbasis $\ket{nlm}$ of $H_0$ 
$E_1^k = =\frac{1}{8m^3c^2}\langle p^4 \rangle_{nlm}$ 
tricks to evaluate matrix element.
$H_0 = \frac{p^2}{2m} - \frac{e^2}{r}$ 
$p^4 = 4m^2(H_0^2 + \frac{2e^2}{r}H_0 + \frac{e^4}{r^2})$ 
$E_k^1=-\frac{1}{2mc^2}$ $(E_n^0)^2+2e^2E_n^0 \langle \frac{1}{r} \rangle_{nlm} + e^4 \langle \frac{1}{r^2} \rangle _{nlm}$    
for $\langle \frac{1}{r} \rangle$ we use virial theorem. $E = \frac{1}{2} \langle V \rangle = \frac{-e^2}{2} \langle \frac{1}{r} \rangle$ . Therefore $\langle \frac{1}{r} \rangle = \frac{1}{n^2 a_0}$ 
$e^4 \langle \frac{1}{r^2} \rangle = \frac{(E_n^0)^4 4n}{l+ \frac{1}{2}}$ (Shankar ex17.3.4)
$H_{SOC}$  need to find the basis states that diagonlize $\vec{L} \cdot \vec{S}$ 
starting with $\ket{nlm,s,m_s}$ where $n=2, s= \frac{1}{2}$ , we have 8 states. 
We can split the Hamiltonian to a 2x2 block for $l=0$
and 6x6 block for $l=1$. Where fhe $l=1$ block can split into a 2x2 block and 4x4 block.
$\vec{J} = \vec{L} + \vec{S}$
$\vec{J}^2 =  \vec{L}^2 + \vec{S}^2 + 2 L \cdot S$. Therefore, we can re-write $\vec{L}\cdot \vec{S} = \frac{1}{2}[j(j+1)-l(l+1)-s(s+1)]$ 
whre $j = l \pm s$ 
$\ket{n=2,l,m,\frac{1}{2},m_S} \rightarrow \ket{n=2,j,m_j,\frac{1}{2},m_s}$ (how to transform? Think Cleb-Gordan coieff)









