## The adiabatic approximation
### The berry phase

When we are studying adiabatic processes, we are talking about processes that are "slow"  where our extrinsic time scale $T_{e}$ is much greater than the intrinsic time scale of the system $T_{i}$ 

For instance, suppose we have a physical pendulum with length $L$ . In this case, the intrinsic time would be $T_{i} = 2\pi \sqrt{ \frac{L}{g} }$ , and as long as the time it takes for us to, let's say change the length of the pendulum $L(t) \to \frac{1}{2} L(t)$ in a large time $T_{e}$ . We then require $T_{i} \ll T_{e}$. 

The trajectory of the physical pendulum in phase space is a ellipse as we have 
$$
\begin{align}
H = \frac{p^{2}}{2m} + \frac{1}{2} m \omega^{2} x^{2} &= E \\ 
\implies \frac{p^{2}}{2mE} + \frac{x^{2}}{\frac{2E}{m \omega^{2}}} &= 1 \\ 
\implies a = \sqrt{ \frac{2E}{m \omega^{2}} }, b &= \sqrt{ 2mE } \\
\implies I = \frac{1}{2 \pi} \cdot \text{Area} &= \frac{ab}{2} \\
= \frac{1}{2}\sqrt{ \frac{2E}{m \omega^{2}}2mE } &= \frac{E}{\omega} 
\end{align}
$$


Note that when we modify the length of the system, we change $\omega$, so $I$ is modified slowly. This is classical example of adiabatic process, but in quantum, we have operators such as 
$$
H = \frac{\hat{p^{2}}}{2m} + \frac{1}{2}m \omega^{2} \hat{x}^{2} \tag{1} 
$$

And suppose the system is in a state of  infinite square well with width $a$. This gives the wave function $\psi_{0}(x) = \sqrt{ \frac{2}{a} } \sin (\frac{\pi}{a} x)$ , and if we slowly increase the width from $a \to 2a$ , we eventually will get the ground state wave function $\psi_{1}(x)= \sqrt{ \frac{1}{a} } \sin\left( \frac{\pi}{2a}x \right)$ , which is just the ground state wave function when we change $a\to 2a$
However, if we change the width of the well rapidly, the wave function will not have enough time to re-adjust, so our wave function will be at a state where it is not an eigenstate of our system. With this intuition, we write down `The adiabatic theorem:`
___


#### The adiabatic theorem:
If H changes "slowly"  from $H(t_{i})$ to $H(t_{f})$, then a particle that start in an eigenstate $\psi_{n}^{i}(t_{i})$ of $H(t_{i})$ remains in the $n$th eigenstate $\psi_{n}^{*}(t_{f})$ of $H(t_{f})$ 

We note that this is only true for discrete energy spectrum where 
$$
\begin{align}
H(t) \psi_{n}(t) &  = E_{n}(t) \psi_{n}(t) \\
H \psi_{n}  & = E_{n}\psi_{n}
\end{align} \tag{2} 
$$

where the intrinsic time scale $\frac{1}{\omega } \approx \frac{\hbar}{E_{n+t}(t)- E_{n}(t)} \ll t_{f} - t_{i}$.
We want to note that the instantaneous $\psi_{n}(t)$ are not solutions to the time- dependent Schrodinger equation, but they still satisfy $\braket{ \psi_{n}(t) | \psi_{m}(t) } = \delta_{mn}$.
___
#### Proof to the adiabatic theorem:
note that our $\psi_{n}$ must also satisfy the time-dependent Schrodinger equation 
$$
i \hbar = \frac{\partial \psi(t)}{\partial t} = H \psi(t)
$$
This means that our $\psi_{n}(0) \to \psi_{n}(t) = \psi_{n}(0) e^{-iE_{n}t/\hbar}$ , which introduces a dynamic phase to our wave function. We will try to find the solution to 
$$
i \hbar \frac{\partial \psi(t)}{\partial t} = H(t) \psi(t) \tag{3} 
$$

However, the solution for $(3)$ can be extremely complicated. We then seek to expand $\psi_{n}(t)$ to the instantaneous equation 
$$
\psi(t) = \sum_{n} c_{n}(t) \psi_{n}(t) e^{i \theta_{n} (t)} \tag{4} 
$$

where $\psi_{n}(t)$ is just the instantaneous eigenstates that satisfy $(2)$, and we also have 
$$
\theta_{n}(t) = -\frac{1}{\hbar} \int_{0}^{t} E_{n}(t') \, dt' \tag{5}  
$$

We then combine $(3),(4)$ and get LHS:
$$
\begin{align}
i \hbar \frac{\partial \psi(t)}{\partial t}  & = i \hbar \sum_{n}[\dot{c}_{n}(t) \psi_{n}(t) e^{i \theta_{n}(t)} + c_{n} \dot{\psi}_{n}e^{i \theta_{n}(t)}+ c_{n}(t) \psi_{n}(t) i \dot{\theta}_{n}(t)e^{i\theta_{n}(t)}] \\
&= i \hbar \sum_{n} [\dot{c}_{n} \psi_{n}+ c_{n} \dot{\psi}_{n}+ i c_{n} \psi_{n} \dot{\theta}_{n}]e^{i \theta_{n}}
\end{align} \tag{6} 
$$


And RHS
$$
\begin{align}
H(t) \psi(t)  & = \sum_{n}c_{n}(t)[H(t) \psi_{n}(t) ]e^{i \theta_{n}(t)} \\
& =\sum_{n} c_{n}(t) E_{n}(t)\psi_{n}(t) e^{i \theta_{n}(t)}  \\
\end{align} \tag{7} 
$$

as we used the simplification that 
$$
\sum_{n} (\dot{c}_{n} \psi_{n}+ c_{n} \dot{\psi}_{n})e^{i \theta_{n}}=0
$$

We then use the orthogonality 
$$
\braket{ \psi_{n}(t) | \psi_{m}(t) }  = \delta_{mn}
$$

to get from the LHS equation 
$$
\begin{align}

\bra{\psi_{m}(t)}  \sum_{n} \dot{c}_{n} \ket{\psi_{n}(t)}  e^{i \theta_{n}} = -\sum_{n} c_{n} \ket{\dot{\psi}_{n}(t)} e^{i \theta_{n}} \\

\sum_{n} \dot{c}_{n}\delta_{mn}e^{i \theta_{n}} = - \sum c_{n} \braket{ \psi_{m}(t) | \dot{\psi}_{n}(t) } e^{i \theta_{n}} \\
\dot{c}_{m} = - \sum_{n} c_{n} \braket{ \psi_{m}(t) | \dot{\psi}_{n}(t) } e^{i \theta_{n}(t) - \theta_{m}(t)} \\
\end{align}
$$

We recognize our instantaneous wave function $\psi_{n}$ mus satisfy:
$$
H(t) \ket{\psi_{n}(t)} = E_{n}(t)\psi_{n}(t)
$$

We take the time derivative 
$$
\dot{H}(t) \ket{\psi_{n}(t)} + H(t) \ket{ \dot{\psi}_{n}(t)} = \dot{E}(t)\ket{\psi(t} + E_{n} \ket{\dot{\psi}_{n}(t)}   
$$

We sandwich this by $\bra{\psi_{m}}$ 
$$
\bra{\psi_{m}} \dot{H} \ket{\psi_{n}}  + \bra{\psi_{m}} H \ket{\dot{\psi}_{n}} 
= \dot{E_{n}}(t) \delta_{mn} + E_{n}(t) \braket{ \psi_{m} | \dot{\psi}_{n} } = \dot{E_{n}}\delta_{mn}+E_{n} \braket{ \psi_{m} | \dot{\psi}_{n} }   
$$

for case $m-n$, we straight up get Feynman- Hellman theorem 

$$
\bra{\psi_{m}} \dot{H} \ket{\psi_{n}}  = \dot{E}_{m} 
$$

and for $m \neq n$, we have 
$$
\bra{\psi_{m}}  \dot{H} \ket{\psi_{n}} = (E_{n} - E_{m}) \braket{ \psi_{m} | \dot{\psi}_{n} } 
$$

where 
$$
c_{m}(t) = - c_{m} \braket{ \psi_{m} | \dot{\psi}_{m} } - \sum_{n \neq m} c_{n} \frac{\bra{\psi_{m}} \dot{H} \ket{\psi_{n}}}{E_{m}-E_{n}} \tag{10} 
$$

However, we assumed that the way we modify our Hamiltonian is significantly slower than the intrinsic energy difference in $(10)$ . Therefore, we can ignore the second term in $(10)$ and get 

$$
c_{m}(t) = -c_{m} \braket{ \psi_{m} | \dot{\psi}_{m} }  = - c_{m} \delta_{m}
$$

where $\delta_{m} \equiv \int \psi_{m} \frac{\partial}{\partial t} \psi_{m}  \, dx$ . After solving the differential equation for $c_{m}$This is called the Berry Phase.