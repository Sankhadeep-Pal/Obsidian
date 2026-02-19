### **11. State de Broglie’s hypothesis and express the de Broglie wavelength in terms of momentum.**

Louis de Broglie proposed that every moving particle possesses both wave and particle characteristics. This means that matter can exhibit wave-like behavior under certain conditions. The wavelength associated with a moving particle is know n as the _de Broglie wavelength_, and it is expressed as:  
$$\lambda = \frac{h}{p}$$ 

where

- $\lambda$= de Broglie wavelength
    
- $h$ = Planck’s constant 6.63×10⁻³⁴ J·s
    
- p = momentum of the particle mv

---

### **12. Derive the expression for de Broglie wavelength in terms of kinetic energy for a non-relativistic particle.**

For a non-relativistic particle,  
 
$$p = \sqrt{2mE_k}$$

where $E_k$  is the kinetic energy and $m$ is the mass of the particle.

Substituting into de Broglie’s relation $$\lambda = \frac{h}{p}$$:  

$$\lambda = \frac{h}{\sqrt{2mE_k}}$$

Hence, the de Broglie wavelength of a particle is inversely proportional to the square root of its kinetic energy.

---

### **13. An electron is accelerated through a potential difference of 100 V. Calculate its de Broglie wavelength.**

**Given:**  
$$e = 1.60\times10^{-19},C ), ( V = 100,V ), ( m_e = 9.11\times10^{-31},kg ), ( h = 6.63\times10^{-34},J·s$$

Kinetic energy gained by the electron:  
$$
E = eV = 1.60\times10^{-19} \times 100 = 1.6\times10^{-17}J
$$
$$   
\lambda = \frac{h}{\sqrt{2mE}} = \frac{6.63\times10^{-34}}{\sqrt{2(9.11\times10^{-31})(1.6\times10^{-17})}} = 1.23\times10^{-10},m  
$$

**Answer:** The de Broglie wavelength of the electron is **0.123 nm**.

---

### **14. A proton and an electron have equal kinetic energies. Determine which has the shorter de Broglie wavelength and by what factor.**

From the expression $\lambda = \frac{h}{\sqrt{2mE}}$, the wavelength is inversely proportional to the square root of the particle’s mass.  
Since a proton is heavier than an electron, it has a shorter wavelength.  
$$  
\frac{\lambda_p}{\lambda_e} = \sqrt{\frac{m_e}{m_p}} = \sqrt{\frac{9.11\times10^{-31}}{1.67\times10^{-27}}} = 0.0233  
$$

Hence, the proton’s wavelength is shorter by a factor of approximately **43 times**.

### **15. Describe the Davisson–Germer experiment and explain how its results confirm de Broglie’s hypothesis.**

In the Davisson–Germer experiment, a beam of electrons was directed at a nickel crystal, and the intensity of reflected electrons was measured at various angles. The observed diffraction pattern was similar to that produced by X-rays, which are known to exhibit wave behavior.

The measured wavelength of the electrons matched the wavelength predicted by de Broglie’s equation $\lambda = \frac{h}{p}$.  
This confirmed that electrons—and therefore all matter—can behave as waves, providing experimental proof of de Broglie’s hypothesis.

---

### **17. What is matter wave? Write some properties of matter wave.**

A _matter wave_ is the wave associated with a moving particle, as proposed by de Broglie. It represents the wave nature of matter.

**Properties of matter waves:**

1. Every moving particle has an associated wavelength given by $$\lambda = \frac{h}{p}$$.

2. The wavelength is inversely proportional to the particle’s momentum.

3. Matter waves can show interference and diffraction.

4. They are not electromagnetic in nature.

5. They disappear when the particle is at rest.


**21. Write the time-independent Schrödinger equation and define all symbols.**

Time-independent Schrödinger equation (nonrelativistic, single particle):  
$$
\hat{H},\psi(\mathbf{r}) = E,\psi(\mathbf{r})  
$$
with the typical Hamiltonian  
$$ 
\hat{H} = -\frac{\hbar^{2}}{2m}\nabla^{2} + V(\mathbf{r}).  
$$

**Definitions**

- $\psi(\mathbf{r})$: wavefunction $stationary state$ as a function of position $\mathbf{r}$.
    
- $\hat{H}$: Hamiltonian operator $total energy operator$.
    
- $E$: energy eigenvalue associated with $\psi$.
    
- $\hbar$: reduced Planck constant, $\hbar = \dfrac{h}{2\pi}$.
    
- $m$: particle mass.
    
- $\nabla^{2}$: Laplacian operator $sum of second derivatives with respect to spatial coordinates$.
    
- $V(\mathbf{r})$: potential energy as a function of position.

---

**22. Physical meaning of $\psi(x,t)$. Significance of $|\psi|^{2}$.**

- $\psi(x,t)$ is a complex amplitude describing the quantum state. It contains _all_ information about the system (up to a global phase) and evolves deterministically under the Schrödinger equation.
    
- **Born interpretation:** $|\psi(x,t)|^{2}$ is the probability density for finding the particle at position (x) at time (t). Explicitly,  
    $$  
    P(x\in \$\$a,b\$\$,t)=\int_a^b |\psi(x,t)|^{2},dx.  
    $$
    
- **Normalization condition:** $\displaystyle\int_{-\infty}^{\infty} |\psi(x,t)|^{2},dx = 1$ for a single particle in all space.
    
- (|\psi|^{2}) is real and nonnegative; physical observables are obtained from (\psi) via operators and expectation values.
    

---

**23. State Heisenberg’s uncertainty principle and its mathematical form for position and momentum.**

General operator form (Robertson relation):  
$$  
\Delta A,\Delta B \ge \frac{1}{2}\big|\langle (\hat{A},\hat{B})\rangle\big|,  
$$  
where $\Delta A=\sqrt{\langle\hat{A}^{2}\rangle-\langle\hat{A}\rangle^{2}}$.

For position $\hat{x}$ and momentum $\hat{p}$ (one dimension) with commutator $(\hat{x},\hat{p})=i\hbar$:  
$$  
\boxed{\Delta x,\Delta p \ge \frac{\hbar}{2}.}  
$$

Alternative often-seen form using (h): $\Delta x,\Delta p \ge \dfrac{h}{4\pi}$ (same as above because $\hbar=h/2\pi$.

Interpretation: simultaneous precise knowledge of position and momentum is limited by a fundamental lower bound; this is not a measurement defect but intrinsic to quantum states.

---

**24. Explain how Schrödinger’s equation is analogous to Newton’s law (F=ma).**

- **Role as an equation of motion:** Newton’s second law (F=ma) (or equivalently $m\ddot{\mathbf{r}} = -\nabla V)$ governs deterministic trajectories of point particles in classical mechanics. Schrödinger’s equation governs deterministic time evolution of the quantum state (wavefunction). Both are fundamental dynamical laws in their domains.
    
- **Energy operator vs classical energy:** The Hamiltonian (\hat{H}) in Schrödinger’s equation plays the role analogous to total energy (H) in classical mechanics; time evolution is generated by the Hamiltonian in both frameworks.
    
- **Ehrenfest theorem (bridge):** Expectation values of quantum operators obey relations resembling Newton’s equations:  
    $$  
    m\frac{d^2}{dt^2}\langle \hat{x}\rangle = -\langle \nabla V(\hat{x})\rangle,  
    $$  
    so the quantum average follows a classical-like equation when quantum fluctuations are small.
    
- **Key difference:** Newton gives trajectories for definite position & momentum. Schrödinger gives a wavefunction whose evolution is deterministic, but measurements yield probabilistic outcomes. Thus analogous in structure (both are evolution laws) but fundamentally different in interpretation and predictions.
    

---

**25. Mathematical form of the Hamiltonian operator used in Schrödinger equation.**

Single nonrelativistic particle (position representation):  
$$  
\boxed{\hat{H} = -\frac{\hbar^{2}}{2m}\nabla^{2} + V(\mathbf{r},t)}  
$$  
Equivalently using momentum operator $\hat{\mathbf{p}} = -i\hbar\nabla$:  
$$  
\hat{H} = \frac{\hat{\mathbf{p}}^{2}}{2m} + V(\mathbf{r},t).  
$$

For (N) particles:  
$$  
\hat{H} = \sum_{i=1}^{N}\frac{\hat{\mathbf{p}}_{i}^{2}}{2m_{i}} + \sum_{i}V_{\text{ext}}(\mathbf{r}_{i}) + \sum_{i<j}V_{\text{int}}(\mathbf{r}_{i},\mathbf{r}_{j}).  
$$

---

**26. Describe the need for Schrödinger equation and applications.**

**Need**

- Classical mechanics fails at atomic/subatomic scales (discrete spectra, tunneling, photoelectric effect, atomic stability). A wave-based quantum law was required to describe probabilities, interference, and quantization.
    
- Schrödinger equation provides a consistent, predictive framework for bound states, scattering, and time evolution of quantum systems.
    

**Key applications**

- Atomic structure and spectral lines (hydrogen energy levels).
    
- Chemical bonding and molecular orbitals (quantum chemistry).
    
- Quantum tunneling (scanning tunneling microscopy, alpha decay, tunnel diodes).
    
- Solid-state physics (band structures, semiconductors, transistors).
    
- Quantum optics and lasers.
    
- Nuclear physics, particle scattering.
    
- Foundations of quantum information and quantum computing (qubit dynamics).
    
- Nanotechnology and materials science.
    

---
