---
layout: post
title: "Quantum process tomography and the transfer tenor method for long-time non-Markovian dynamics"
category: Science
tags: [Open system, Transfer tensor, Quantum dynamics]
tex: true
author: Linus
---

Predicting long-time dynamics from short-time information is a promising way of studying how equilibrium is approached for an open quantum system starting from a non-equilibrium initial condition. 

This post discusses one of the prediction methods for long-time open system dynamics, the transfer tensor method (TTM)<sup id="footnote-ref-1">[\[1\]](#footnote-2)</sup>. The TTM is based on, (i) the Nakajima-Zwanzig equation equation of an open quantum system Eq. \eqref{eq:1}, and (ii) the assumption that the state of the open system at time $t$ is barely correlated with the state at $t'$ if $\|t-t'\|$ is greater than a certain threshold. Let's start from the Nakajima-Zwanzig equation of an open system<sup id="footnote-ref-2">[\[2\]](#footnote-2)</sup>:

<mj>
\begin{equation}
\label{eq:1}
\frac{d}{d t} {\rho}(t)=-\frac{i}{\hbar} \mathcal{L}_{s} {\rho}(t)-\int_{0}^{t} d \tau\, \mathcal{K}(\tau) {\rho}(t-\tau)
\end{equation}
</mj>

where $\mathcal{L}\_{s}$ is the Liouville operator corresponding to the system part of the system-bath Hamiltonian, and $\rho(t)$ is the system reduced density matrix. The memory kernel $\mathcal{K}(\tau)$ measures how correlated a state $\rho(t)$ is to a previous state $\rho(t-\tau)$. This this equation can be discretized on time grids $(0, \delta, 2\delta, \ldots, N\delta)$ as follows (superscripts below are the time grids: $\mathcal{K}\_{n}=\mathcal{K}({n\delta})$  and such):

<mj>
\begin{equation}
\label{eq:2}
{\rho}_{N} = (1- \frac{i}{\hbar} \mathcal{L}_{s}\delta)\rho_{N-1} -\sum_{n=1}^{N} \delta^2\mathcal{K}_{n} \rho_{N-n}.
\end{equation}
</mj>

<figure id="fig-1">
  <img src="{{ '2022-04-08-quantum-process-tomography-and-transfer-tensors.png' | prepend:'/upload/posts/' | relative_url }}" alt="transfer tensor">
  <figcaption><b>Figure 1.</b> The discretized integral in Eq. \eqref{eq:1}.</figcaption>
</figure>

This means, if we know that memory kernel $\mathcal{K}(t)$ decays to zero after a certain time $t_\mathrm{max}$, we can use the memory kernel and reduced density matrices before $t_\mathrm{max}$ to calculate the reduced density matrix to as long a time as we want. For example, if $\mathcal{K}(t>10\delta)=0$, we can use a sequence of initial density matrices $\rho\_0,\ldots,\rho\_{9}$ and $\mathcal{K}\_{1},\ldots,\mathcal{K}\_{10}$ to calculate ${\rho}\_{10}$. Again, based on ${\rho\_{1}},\ldots,{\rho\_{11}}$ (just obtained in the last step) and $\mathcal{K}\_{1},\ldots,\mathcal{K}\_{10}$ we can obtain ${\rho}\_{11}$. This calculation can go on and on until we get the density matrix at a desired long enough time.

The question is how to obtain the initial sequence ${\rho\_{1}},\ldots,{\rho\_{10}}$ and $\mathcal{K}\_{1},\ldots,\mathcal{K}\_{10}$. The density matrix part can be easily obtained by simulating the open system with an desired initial condition. The memory kernel is a bit more difficult to obtain. To calculate $\mathcal{K}\_n$, we first note that Eq. \eqref{eq:2} can be rewritten as

<mj>
\begin{align}
\begin{split}
\rho_{1}  = \mathcal{E}_1\rho_0 \equiv &(1- \frac{i}{\hbar} \mathcal{L}_{s}\delta - \mathcal{K}_1\delta^2){\rho}_0  \\
\rho_{2} = \mathcal{E}_2\rho_0 \equiv & (1- \frac{i}{\hbar} \mathcal{L}_{s}\delta - \mathcal{K}_1\delta^2){\rho}_{1} - \mathcal{K}_2\delta^2 \rho_{0} \\
                                    = &  (1- \frac{i}{\hbar} \mathcal{L}_{s}\delta - \mathcal{K}_1\delta^2)\mathcal{E}_1\rho_0 + \mathcal{K}_2\delta^2 \rho_{0} \\
\rho_{N} = \mathcal{E}_N\rho_0 \equiv & (1- \frac{i}{\hbar} \mathcal{L}_{s}\delta - \mathcal{K}_1\delta^2){\rho}_{N-1} - \sum_{n=2}^N \mathcal{K}_n\delta^2 \rho_{N-n} \\
                                    = & (1- \frac{i}{\hbar} \mathcal{L}_{s}\delta - \mathcal{K}_1\delta^2)\mathcal{E}_{N-1}\rho_0 - \sum_{n=2}^{N-1} \mathcal{K}_n\delta^2 \mathcal{E}_{N-n}\rho_{0} - \mathcal{K}_N\delta^2\rho_{0}
\end{split}
\end{align}
</mj>

where we define the Liouville space matrix that maps $\rho\_0$ to $\rho\_N$ to be $\mathcal{E}\_N$ and $\mathcal{E}\_0=1$. This matrix doesn't depend on the initial state $\rho\_0$ (e.g. $\mathcal{E}\_1=1- \frac{i}{\hbar} \mathcal{L}\_{s} - \mathcal{K}\_1$). If $\mathcal{E}\_n$ can be obtained, the memory kernels can be solved for iteratively: 

\begin{equation}
\mathcal{K}\_n\delta^2 = \mathcal{E}\_n - (1- \frac{i}{\hbar} \mathcal{L}\_{s}\delta - \mathcal{K}\_1\delta^2) -\sum\_{m=2}^{n-1}\mathcal{K}\_m\delta^2\mathcal{E}\_{n-m}.
\end{equation}

To simplify notations, let's define $T\_1=1- \frac{i}{\hbar} \mathcal{L}\_{s}\delta - \mathcal{K}\_1\delta^2$, $T\_2=\mathcal{K}\_2\delta^2$, ..., $T\_N = \mathcal{K}\_N\delta^2$.

If we regard a density matrix as a vector, then the map $\mathcal{E}\_n$ is a matrix. The matrix can be constructed explicitly if we know the effect of the matrix on each basis vector. To this end, we work in the Liouville space, i.e., the elements of a $D\times D$ density matrix $\{\rho\_{nm}\}$ are represented by a vector $(v\_0,\ldots,v\_k,\ldots,v\_{N^2-1})$ with $k=n+mD$. Assuming $D=2$, the basis for the $N^2$ dimensional vector space can be chosen as $(1,0,0,0)^T, (0,1,0,0)^T, (0,0,1,0)^T$, $(0,0,0,1)^T$. They corresponds to the basis of the density matrix $\|0\rangle\langle0\|$, $\|0\rangle\langle1\|$, $\|1\rangle\langle0\|$, and $\|1\rangle\langle1\|$. These basis vectors, if regarded as initial conditions for Eq. \eqref{eq:1} , will be propagated to time $\delta,2\delta,\ldots,9\delta$. The resulting vectors at these time grid points, after transposition, are in fact the rows of the map matrix $\mathcal{E}_1,\ldots,\mathcal{E}\_9$, respectively:

<mj>
\begin{equation}
\mathcal{E}_n
\begin{pmatrix}
1\\ 0\\ 0\\ 0
\end{pmatrix}=
\begin{pmatrix}
E_{00} & E_{01} & E_{02} & E_{03}\\
E_{10} & E_{11} & E_{12} & E_{13}\\
E_{20} & E_{21} & E_{22} & E_{23}\\
E_{30} & E_{31} & E_{32} & E_{33}\\
\end{pmatrix}
\begin{pmatrix}
1\\ 0\\ 0\\ 0
\end{pmatrix} = 
\begin{pmatrix}
E_{00} \\ E_{01} \\ E_{02} \\ E_{03}
\end{pmatrix}.
\end{equation}
</mj>

Using the basis vectors as four different initial conditions, we can obtain the full information of the maps $\mathcal{E}\_n$. This is called quantum process tomography. But there's a problem with the above choice of basis vectors: $(0,1,0,0)$ and $(0,0,1,0)$ are not valid (vectorized) density matrices. $(0,1,0,0)$ corresponds to $\|0\rangle\langle1\|$; $\|0\rangle\langle1\|$ doesn't satisfy the hermitian condition for density matrices. The solution to this problem is we can use other basis that satisfies the hermitian conditions. Define $\|+\rangle=\frac{\|0\rangle+\|1\rangle}{\sqrt{2}}$ and $\|-\rangle=\frac{\|0\rangle+i\|1\rangle}{\sqrt{2}}$; one has

<mj>
\begin{align}
\begin{split}
|0\rangle\langle1| = |+\rangle\langle+| + i|-\rangle\langle-| - \frac{1+i}{2}(|0\rangle\langle0|+|1\rangle\langle1|)\\
|1\rangle\langle0| = |+\rangle\langle+| - i|-\rangle\langle-| - \frac{1-i}{2}(|0\rangle\langle0|+|1\rangle\langle1|)
\end{split}
\end{align}
</mj>

The basis $\|0\rangle\langle0\|$, $\|1\rangle\langle1\|$, $\|+\rangle\langle+\|$, and $\|-\rangle\langle-\|$ all are valid density matrices; therefore, they can be used as valid initial conditions for Eq. \eqref{eq:1}. The effects of $\mathcal{E}_n$ on $\|0\rangle\langle1\|$ and $\|1\rangle\langle0\|$ are the linear combinations of $\mathcal{E}_n(\|+\rangle\langle+\|)$, $\mathcal{E}_n(\|-\rangle\langle-\|)$, $\mathcal{E}_n(\|0\rangle\langle0\|)$, and $\mathcal{E}_n(\|1\rangle\langle1\|)$.

Note: $\mathcal{E}_n(\|0\rangle\langle1\|)$ doesn't equal to the complex conjugate of  $\mathcal{E}_n(\|1\rangle\langle0\|)$, but equals to the Hermitian transpose of $\mathcal{E}_n(\|1\rangle\langle0\|)$. As a result, in the Liouville space, the vector corresponding to $\mathcal{E}_n(\|0\rangle\langle1\|)$ is **absolutely not** the complex conjugate of the vector version of $\mathcal{E}_n(\|1\rangle\langle0\|)$.


<hr style="height: 1px;width: 50%;background-color: black;margin-bottom: 5px;">
<ol style="font-size: smaller;">
  <li id="footnote-1">
    Cerrillo, Javier, and Jianshu Cao. Non-Markovian dynamical maps: numerical processing of open quantum trajectories. <i>Phys. Rev. Lett.</i> <b>112</b>(11) (2014), 110401. <a href="#footnote-ref-1" title="go back">↩</a>
  </li>
  <li id="footnote-2">
    Shi, Qiang, and Eitan Geva. A new approach to calculating the memory kernel of the generalized quantum master equation for an arbitrary system–bath coupling. <i>J. Chem. Phys.</i> <b>119</b>(23) (2003): 12063-12076. <a href="#footnote-ref-2" title="go back">↩</a>
  </li>
</ol>