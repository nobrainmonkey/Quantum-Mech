## Time-dependent perturbation theory 
$$
\begin{align}
H  & = H_{0}+\lambda H_{1}(t) \\
\ket{\psi(0)}  & =\ket{i} \\
\end{align}
$$
and we want to solve for $\ket{\psi(t)}$ for first degree in $\lambda H_{1}$
$$
\begin{align}
P_{i\to f} & = \lvert \braket{ f | \psi(t) }  \rvert ^{2} \\
P_{i \to f}(t) & =\frac{\lvert V_{fi} \rvert^{2}}{\hbar^{2}} \left\lvert  \frac{1-e^{i (\omega_{fi}+\omega)t}}{\omega_{fi}+\omega} +\frac{1-e^{i(\omega_{fi}-\omega)t}}{\omega_{fi}-\omega} \right\rvert ^{2} \tag{1} 
\end{align}
$$
With the following Initial condition:
$$
\begin{align}
H_{1}(t)  & =2V\cos (\omega t) \Theta(t)\\
h \omega_{fi}  & = E_{f} - E_{i} \\
\bra{f} H \ket{i}  & \equiv V_{fi}
\end{align}
$$
___
## Sinusoidal Potential
Let us understand $(1)$ in the case of two discrete levels with sinusoidal perturbation $\omega >0$.

We fix observation time $t$ and vary perturbation frequency $\omega$. Note that it seems if $\omega = \pm \omega_{fi}$ we would observe resonance.

Now we have two cases:
	1. if $E_{f}>E_{i}$ resonance happens when $\omega \to \omega_{fi}>0$. This is called **resonant absorption**. 
	2. if $E_{f} < E_{i}$ resonance happens when $\omega \to -\omega_{fi}>0$. This is called **resonant emission.**

Without loss of generality, let us only consider the case of resonant absorption.

Let us define 
$$
\begin{align}
\left\lvert  \frac{1-e^{i (\omega_{fi}+\omega)t}}{\omega_{fi}+\omega} \right\rvert  & \equiv A_{+}  \\
\left\lvert  \frac{1-e^{i (\omega_{fi}+\omega)t}}{\omega_{fi}-\omega} \right\rvert  & \equiv A_{-}
\end{align}
$$
Note that we can the following math equation is true:
$$
\frac{1-e^{i \theta t}}{\theta}= - i e^{i \theta t/2} \frac{\sin\left( \frac{\theta t}{2} \right)}{\frac{\theta}{2}}
$$
This gives
$$
\begin{align}
A_{\pm} = -i e^{i (\omega_{fi}\pm \omega )t/2} \frac{ \sin\left[ \frac{(\omega_{fi}\pm \omega)t}{2} \right] }{\frac{\omega_{fi}\pm \omega}{2}}
\end{align}
$$
note that We only consider the $A_{-}$ term for the absorption case. Then, for $\lvert \omega-\omega_{fi} \rvert \ll \omega_{f}$, we get 
$$
P_{i \to f}(t:\omega) \approx \frac{\lvert V_{fi} \rvert^{2} }{\hbar^{2}} \left\lvert \frac{ \sin\left[ \frac{(\omega_{fi}- \omega)t}{2} \right] }{\frac{\omega_{fi}- \omega}{2}} \right\rvert^{2}
$$
Note that the central maxima width of the diagram if $\frac{4\pi}{t}$, the second peak is less than $5\%$ of the central peak.
And finally, when $\omega\to \omega_{fi}, P\to \frac{\lvert V_{fi} \rvert^{2} t^{2}}{\hbar^{2}}$. 
___
## Validity of our result
1. Near $\omega$ of absorption resonance, $\lvert A_{+}(\omega) \rvert \ll \lvert A_{-}(\omega ) \rvert$
	1. $2 \lvert \omega _{f} \rvert \gg \frac{4\pi}{t}$. This means the two peaks are well-separated
	2. This also means $t \gg \frac{1}{\lvert \omega_{ft} \rvert} \approx \frac{1}{\omega}$ 
2. $P_{i\to f}(t;\omega=\omega_{fi}) = \frac{\lvert V_{fi} \rvert^{2}}{\hbar^{2}} t^{2}$, but our first degree perturbation requires $P_{i\to f} \ll 1$, so $t\ll \frac{\hbar}{\lvert V_{fi} \rvert}$  
Putting 1. and 2. together, we have 
$$
\frac{1}{\omega}\approx \frac{1}{\lvert \omega_{fi} \rvert } \ll t \ll \frac{\hbar}{\lvert V_{fi} \rvert }
$$
Therefore, we also have $\hbar \lvert \omega_{fi} \rvert \gg \lvert V_{fi} \rvert$. This means the separation of energy levels must be much larger than our perturbation potential energy, which makes sense!