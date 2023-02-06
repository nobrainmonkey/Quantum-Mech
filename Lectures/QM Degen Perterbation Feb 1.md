
## Van der Walls Probblem Set up
Scale of electron chatrge ~ $a_0$ 
Distance between the two charges $= R \hat{n}$  , we have $R >> a_0$
$H_0 = H_A + H_B$ is the none perterbed Hamiltonian
$H = H_0 + W$ where W is the perterbation term, which is the dipole-dipole interaction.

let $\vec{r_a}$ represents the vector pointing from proton A to electron A
let $\vec{r_b}$ represetns the vector pointing from proton B to electron B

From classical E&M
$\vec{\mu_A} = e \vec{r_a}$ 
$\vec{\mu_b} = e \vec{r_b}$ 
$W = \frac{\vec{\mu_A} \cdot \vec{\mu_b}-3(\vec{\mu_A}\cdot \hat{n})(\vec{\mu_B}\cdot \hat{n})}{R^3}$ 

let 
$\hat{n} = \hat{z}\rightarrow \frac{e^2}{R^3}(x_ax_b+y_ay_b-2z_az_b)$ 
and the unperterbed eigenstate $\ket{\psi_{nlm}^A}\ket{\psi_{n'l'm'}^B}$ 
and Energy perterbation $E = E_n^0 +E_{n'}^0$

1st order term is zero : why? (symmetrical in $\hat{R}$, odd $R$ ?)
2nd order term $\rightarrow -\frac{C}{R^6}$ , find dimension for $C$

## Degenerate Perterbation Theory 
Earlier formula $\ket{n}=\sum_{m \neq n} \frac{\bra{m_0} H_1 \ket{n_0}}{E_n^0 - E_m^0} \ket{m_0}+ ...$ 
Note that his __cannot__ be used when $E_n^0 =E_m^0$ 
Now suppose our Hamiltonian have degenerate eigenenergy
Let $H_0 \ket{n_0,r}=E_n^0 \ket{n_0, r}$ where $r$ label the degenerate states and $r \in \{1,2,...,D\}$ 

Thoght process: We stratigically choose a particuliar linear combination of $\ket{n_0 ,r}$ such that the matrix elements corresponding to problematic demoninator also vanish.

We will show next that this is accomplished by:
choose $\ket{\psi_{n,r}^0} =\sum_s c_{r,s} \ket{n_0,s}$ s.t. $\bra{\psi_{n,r}^0} H_1 \ket{\psi_{n,r'}^0} = E'_n\delta_{r,r'}$  

Proof:
let $\ket{\psi_{n,r}^0}=\sum_s c_{r,s} \ket{n_0,s}$ 
$\bra{\psi_{r,s}} \ket{\psi_{r',s}}=\delta_{r,r'}$ 
LHS = $\sum_{s,s'} c^*_{r,s}c_{r',s'}\braket{n_0,s|n_0,s'}= \sum _s c^*_{r,s}c_{r',s} = \delta_{r,r'}$  (1)
Need to solve 
$(H_0+\lambda H_1)(\ket{\psi_{n,r}^0} + \lambda \ket{\psi_{n,r}^1}) = (E_n^0+\lambda E_n^1)(...)$

0th ordr in $\lambda$ : $H_0 \ket{\psi_{n,r}^0} = E_0 \ket{\psi_{n,r}^0}$ 
1st order in $\lambda$: $H_0 \ket{\psi_{n,r}^1} + H_1 \ket{\psi_{n,r}^0}= E_n^0 \ket{\psi_{n,r}^1} + E_n^1 \ket{\psi_{n,r}^0}$ 
1st term of LHS = $\braket{\psi^0_{n,s}H_0 |\psi^1_{n,r}}=E_n^0 \braket{\psi^0_{n s} |{\psi^1_{n,r}}}= E_n^0 \delta_{s,r}$    
2nd term of LHS = $\braket{\psi^0_{n,s}H_1 \ket{\psi^1_{n,r}}=E_n^1 \braket{\psi^0_{n s} |\psi^1_{n,r}}}= E_n^1 \delta_{s,r}$ , which is just (1)

### Example: Stark-effect of the n=2 state of H atom





$H = H_0 + H_1$ , $H_1 = e E r \cos{\theta}$ 
Unperterbed eigenstates: $\ket{2,0,0},\ket{2,1,0},\ket{2,1,1},\ket{2,1,-1}$ 
with $E_2 =-\frac{1}{4}(\frac{me^4}{2\hbar^2})$ , which means energy is degenerate

will see that 

$H_1 = \begin{pmatrix} 0 & \Delta & 0 & 0 \\ \Delta & 0 & 0& 0 \\0&0&0&0 \\0&0&0&0 \end{pmatrix}$ 
Note that: 
1. $\bra{nlm} H_1 \ket{n',l',m'} \neq 0$ only for $m=m'$ 
This is because for $\phi$ term for the inneerprocut,  we have the intergral $\int_0 ^{2\pi} e^{-i(m-m') \phi} = 2\pi \delta_{m,m'}$ 
2. $\bra{n,l,m}H_1\ket{n',l',m'}\neq 0$ only for $l'=l\pm 1$  


  