---
layout: post
title: Thermo-Field Dynamics and the Mixed Initial States
category: Science
tags: [Quantum mechanics, Mixed initial states, Quantum dynamics]
img: "2020-12-31-thermo-field-dynamics-and-the-mixed-initial-states.png"
strip: "2020-12-31-thermo-field-dynamics-and-the-mixed-initial-states-strip.png"
tex: true
author: Linus
---

When simulating the dynamics of open quantum systems, one often assumes a pure initial state of the system part. The validity of the assumption, of course, depends on the experimental realization. In most of the excitation energy transfer experiments, a pure initial state is a faithful representation of the system because the coherent light that excites molecules makes the wave-function of the system collapse to a certain state, hence factorizes the system-environment density matrix. The factorized density matrix is $\rho(t=0)=\rho_\mathrm{sys}(0)\otimes\rho_\mathrm{env}(0)$and the density matrix of the system at time zero (initial state)$\rho_\mathrm{sys}(t=0)$ is a pure-state in this case.

The lights in nature, however, are not always coherent. For example, the light of the sun, which is the energy source of the light-harvesting activities in plants, is not coherent. Incoherent lights don't always generate a pure state [\[1\]](#reference-1). Therefore It is relevant to study the relaxation dynamics of the system starting from a mixed initial state. A very useful formalism called *thermo-field dynamics* can handle mixed states by mapping them to pure states. Once a mixed state is mapped to a pure state, all of the conventional numerical methods designed for the Schroedinger equation can be applied to simulate the relaxation dynamics. In the following, the thermo-field formalism is introduced.

Consider an arbitrary time-dependent density matrix $\rho(t)$. The basis of the density matrix is eigenstates $\|n\rangle$ of the system Hamiltonian $H$. The expectation value of an observable $A$ can be obtained from the trace formula $\mathrm{Tr}(\rho A)$. There exists a composite pure state

\begin{equation}
|{\psi_\rho(t)}\rangle=\rho^{1/2}\otimes \mathrm{I}\cdot \sum_{n,n'}|{n}\rangle\otimes |{n'}\rangle
\end{equation}
that can produce the same expectation value by the normal average formula $\langle{\psi_\rho(t)\|A\|\psi_\rho(t)}\rangle$. Here $\hat{\mathrm{I}}$ is the identity operator in the space spanned by $\{|n'\rangle\}$ and $\|n'\rangle$ is a copy of state $\|n\rangle$. 

What's left is to study the time evolution of the state $\|\psi_\rho(t)\rangle=\rho^{1/2}\otimes \mathrm{I}\cdot \sum_{n=n'}\|n\rangle\otimes \|n'\rangle$. We first note the dynamics of the density matrix are governed by the von Neumann equation 

\begin{equation}
i\hbar \frac{\partial \rho}{\partial t} = H\rho - \rho H.
\end{equation}

Then we directly differentiate the state $\|\psi_\rho(t)\rangle$ with respect to the time $t$ and put the von Neumann equation in the result. We have [\[2\]](#reference-2)

\begin{equation}
i\hbar \frac{\partial |{\psi_\rho(t)}\rangle}{\partial t} = (H\rho^{1/2} - \rho^{1/2} H)\sum_{n=n'}|{n}\rangle\otimes |{n'}\rangle
.
\end{equation}

Expanding the equation above, the first term $H\rho^{1/2}\sum_{n=n'}\|n\rangle\otimes \|n'\rangle$ is equal to $H \|{\psi_\rho(t)}\rangle$ by definition. The second term is $-\rho^{1/2} H\sum_{n,n'}\|{n}\rangle\otimes \|{n'}\rangle =- \rho^{1/2} \sum_{n,n'}E_n\|{n}\rangle\otimes \|{n'}\rangle$. It can be rewritten in new way. Noting the fact the $\|{n'}\rangle$ is a copy of $\|{n}\rangle$, one can replace $E_n$ by $E_{n'}$ without affecting the result. Thus,

\begin{align}
\begin{split}
-\rho^{1/2} H\sum_{n=n'}|{n}\rangle\otimes |{n'}\rangle
=&-\sum_{n=n'}E_n(\rho^{1/2}|{n}\rangle)\otimes |{n'}\rangle\\\\\
=&-\sum_{n=n'}E_{n'}(\rho^{1/2} |{n}\rangle)\otimes |{n'}\rangle\\\\\
=&-\sum_{n=n'}(\rho^{1/2} |{n}\rangle)\otimes (E_{n'}{n'}\rangle)\\\\\
=&-\sum_{n=n'}(\rho^{1/2} |{n}\rangle)\otimes (\tilde{H}|{n'}\rangle)\\\\\
=&-\tilde{H}\rho^{1/2}\sum_{n=n'} |{n}\rangle\otimes {n'}\rangle\\\\\
=&-\tilde{H}|{\psi_\rho(t)}\rangle\\\\\
\end{split}
\end{align}

where $\tilde{H}$ is a copy of $H$ and it operates on the duplicate Hilbert spanned by $\|{n'}\rangle$.

Summarizing all the results above, we can conclude that the pure state $\|{\psi_\rho(t)}\rangle$, which is a pure counterpart of the midex state $\rho(t)$, evolves according to the new Schroedinger equation,

\begin{equation}
i\hbar \frac{\partial |{\psi_\rho(t)}\rangle}{\partial t} = (H-\tilde{H}) |{\psi_\rho(t)}\rangle
\end{equation}

in the composite Hilbert space. Solving this equation can provide us the necessary information to obtain the expectation values.

Although the density matrix $\rho$ is mixed, the formalism we introduced above can map it to pure state in a doublet Hilbert space and avoid working with the density matrices. 


## References

<ol>
  <li id="reference-1">
    Brumer, P. (2018). Shedding (incoherent) light on quantum effects in light-induced biological processes. <a href="https://doi.org/10.1021/acs.jpclett.8b00874">The journal of physical chemistry letters, 9(11), 2946-2955</a>.
  </li>
    <li id="reference-2">
    Suzuki, M. (1991). Emerging broken symmetry in space and time. In <i>Thermal Field Theories</i> (pp. 5-15). Elsevier.
  </li>
</ol>