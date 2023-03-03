## Recap:
We have the incident wave 
$$
\psi_{k} (\vec{r}) \sim_{r\to \infty} e^{ikz} + f(\theta) \frac{e^{ikr}}{r}
$$
and scattering amplitude
$$
f(\theta) = \frac{1}{k} \sum_{l=0}^{\infty} (2l+1) \left[ \frac{e^{2 i \delta_{l}}-1}{2i} \right] P_{l}(\cos \theta)
$$
Where all the information are stored in the scattering phase shift. We will need to calculate $\delta_{l}$ given $V(r)$, where $k$ is $E$ dependence. We can then write :

$\sigma(\theta) = | f(\theta)|^2$

Note that we can re-write the $\delta_{l}$ component in $(2)$ as
$$
\left[ \frac{e^{i 2 \delta_{l}}-1}{2i} \right] = e^{i\delta_{l}} \sin\delta_{l} = \frac{1}{\cot \delta_{l} -i}
$$

Now, we realize that there are an infinite number of $\delta_{l}$ to calculate. However, we will see that only "small $l$" (often only $l=0$)  dominates "low energy scattering".
____
## Example: Hard Sphere Potential
Hard Sphere potential is defined as:
$$
\begin{align}
V(r)= 0 \ \text{for} \ r&>0 \\
V(r) =  \infty \ \text{for} \ r&\leq 0
\end{align}
$$

and we wrote out last time that, at $r> r_{0}$
$$
R_{l}(r) = A_{l}j_{l}(kr) + B_{l}n_{l}(kr) \tag{1}
$$

with boundary condition $R_{l}(r_{0})= 0$. This give:
$$
\frac{B_{l}}{A_{l}}= -\frac{j_{l}(kr)}{n_{l}(kr)} \tag{2}
$$
When $r\to \infty$,we have 
$$
R_{l}(kr) \sim_{r\to \infty} \frac{1}{kr} \left[ A_{l} \sin\left( kr-l \frac{\pi}{2} \right)  - B_{l} \cos\left( kr- l \frac{\pi}{2} \right)\right]  =\frac{\sqrt{ A_{l}^2 +B_{l}^2}}{kr} \sin\left( kr - \frac{l\pi}{2} + \delta_{l} \right) \tag{3}
$$

where 
$$
\delta_{l}(k) = \arctan\left( - \frac{B_{l}}{A_{l}} \right) \tag{4}
$$

Combine $(4)$ with $(2)$, we have 
$$
\delta_{l}(k) = \arctan\left( \frac{j_{l}(kr_{0})}{n_{l}(kr_{0})} \right) \tag{5}
$$

Hard sphere scattering solved!
Note: our scale for low energy is when
$$
kr_{0} \ll 1 \implies E \ll \frac{\hbar^2}{mr_{0}^2} \tag{6}
$$

We recall that for $kr_{0} \ll 1$:
$$
\begin{align}
j_{l}(kr_{0}) &\sim \frac{x^l}{(2l +1)!!} \\
n_{l}(kr_{0}) &\sim - \frac{(2l+1)!!}{x^{l+1}} \tag{7}
\end{align}
$$

Combine $(7)$ and $(4)$ gives:
$$
\tan \delta_{l} \approx \delta_{l} \approx -(\alpha) (kr_{0})^{2l+1} \tag{8}
$$

Note that when $k\to 0$, higher $l$  results in phase shift approaches to 0 more rapidly. Therefore, $l=0$ dominates. We have 
$$
\delta_{0}(k) = -kr_{0} \tag{9}
$$

Which is a negative number. This make sense because $\delta_{0} < 0$ for a repulsive potential, as our wave is pushed outward.

We then seek to compute $f_{l=0}(\theta)$ . Using equation from the Recap section, we get 
$$
f_{l=0}(\theta) = \frac{1}{k} e^{i\delta_{0}}\sin(\delta_{0}) =\frac{1}{k} e^{-i k r_{0}}\sin(k r_{0}) \sim r_{0} \tag{10}
$$

Therefore, we have 
$$
\sigma(\theta) \approx_{kr_{0} \ll 1} | f_{0}(\theta)|^2 = r_{0}^2
$$

So $\sigma_{tot} = \frac{4\pi}{k^2} \sin^2 \delta_{0} \to 4 \pi r_{0}^2$ ! What a satisfying result!

___
## Example: Scattering Resonances & S- Wave Scattering Length $a_{s}$
We showed that for $l=0$ , we can write 
$$
f_{0} = \frac{1}{k} \frac{1}{\cot \delta_{0}(k) -1} \tag{11}
$$

We can show that in general, 
$$
\lim_{ k \to 0 } k \cot\delta_{0}(k) = -\frac{1}{a_{s}} + O(k^2 R_{0}) \tag{12}
$$

where $a_{s}$ defines the scattering length for the range of potential $R_{0}$ such that $kR_{0} \ll 1$ (check for hard sphere case where $a_{s} = r_{0}$).

With $(12)$ combined with $(11)$, we have, when $k\to 0$
$$
\begin{align}
f_{0} &\approx \frac{1}{-\frac{1}{a_{s}}+ik} \\
\implies\sigma_{tot} & = 4 \pi |f_{0}|^2 = \frac{4 \pi a_{s}^2}{1+ k^2 a_{s}^2} \tag{13}
\end{align}
$$

Note that if $a_{s}$ is finite,  $\sigma_{tot} \approx 4 \pi a_{s}^2$ . But if $a_{s}$ diverges, we have$\sigma_{tot} \approx \frac{4\pi}{k^2}=$ unitary bound. (We must have conservation of probability) .

### Question: How to make $a_{s} \to 0$ ?
Simplest example: we have a finite square well with depth $-V_{0}$ from $0$ to $r_{0}$ satisfying $kr_{0} \ll 1$. As we we keep decreasing the well, bound we have more bound states appearing. We can show that the graph of $\frac{a_{s}}{r_{0}}$ v.s. $K_{0} r_{0}$ where $K_{0} = \sqrt{\frac{2m|V_{0}|}{\hbar^2}}$ has the behavior
![[Pasted image 20230303122537.png]](note: this is not $\cot$)
And the corresponding $\sigma_{tot}$ v.s. $K_{0} r_{0}$ looking like
![[Pasted image 20230303122828.png]]