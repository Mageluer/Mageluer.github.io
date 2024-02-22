---
layout: post
title: "The Fermi's golden rule electron transfer rate for a multi-state system"
category: Science
tags: [Electron transfer, Quantum dynamics]
tex: true
author: Linus
---

A vibronic Hamiltonian of a 3-state electron-transfer system with a single donor and two acceptors is $\hat{H}_0+\hat{V}$.

\begin{align}
\begin{split}
\hat{H}\_{0}&=\hat{h}\_{a}\left\|a\right\rangle \left\langle a\right\|+\hat{h}\_{b}\left\|b\right\rangle \left\langle b\right\|+\hat{h}\_{c}\left\|c\right\rangle \left\langle c\right\|\\\\\
V&=g\_{ab}\left|a\right\rangle \left\langle b\right|+g\_{ac}\left|a\right\rangle \left\langle c\right\|+g\_{bc}\left\|b\right\rangle \left\langle c\right\|+h.c.
\end{split}
\end{align}

In this Hamiltonian, $\|a\rangle$ is the donor state and $\|b\rangle$ and $\|c\rangle$ are the two acceptor states. If the electronic couplings among $a$, $b$ and $c$ are small, the electron transfer rate can be caluated by using Fermi's golden rule. To to this, we turn to the interaction picture and then calculate the propogator up to the second order.

The Hamiltonian in the interaction picture $V\_{I}(t)=e^{i\hat{H}\_0t}\hat{V}e^{-i\hat{H}\_0t}$ is

\begin{align}
\begin{split}
V\_{I}(t) & = g\_{ab}e^{i\hat{h}\_{a}t}e^{-i\hat{h}\_{b}t}\left\|a\right\rangle \left\langle b\right\|+g\_{ab}^{\*}e^{i\hat{h}\_{b}t}e^{-i\hat{h}\_{a}t}\left|b\right\rangle \left\langle a\right\|\\\\\
+& g\_{ac}e^{i\hat{h}\_{a}t}e^{-i\hat{h}\_{c}t}\left\|a\right\rangle \left\langle c\right\|+g\_{ac}^{\*}e^{i\hat{h}\_{c}t}e^{-i\hat{h}\_{a}t}\left|c\right\rangle \left\langle a\right\|\\\\\
+& g\_{bc}e^{i\hat{h}\_{b}t}e^{-i\hat{h}\_{c}t}\left\|b\right\rangle \left\langle c\right\|+g\_{bc}^{\*}e^{i\hat{h}\_{c}t}e^{-i\hat{h}\_{b}t}\left\|c\right\rangle \left\langle b\right\|.
\end{split}
\end{align}

The corresponding propagator is

\begin{equation}
\hat{U}\_{I}(t)=1-i\int\_{0}^{t}\hat{V}\_{I}(t)dt'-\int\_{0}^{t}dt'\int\_{0}^{t'}dt^{\prime\prime}\hat{V}\_{I}(t')\hat{V}\_{I}(t'')+\cdots
\end{equation}

The population at the state $\left\|a\right\rangle$ is (assuming the initial nuclear equilibrium at the potential energy surface of $\left\|a\right\rangle$)

\begin{equation}
P\_{a}(t)=\left\langle \phi\_{0}\right\|\left\langle a\right\|\hat{U}\_{I}^{\dagger}(t)\left\|a\right\rangle \left\langle a\right\|\hat{U}\_{I}(t)\left\|a\right\rangle \left\|\phi\_{0}\right\rangle 
\end{equation}

The quantity in the middle is

\begin{align}
\begin{split}
\left\langle a\right\|\hat{U}\_{I}(t)\left\|a\right\rangle = &1-i\int\_{0}^{t}\left\langle a\right\|\hat{V}\_{I}(t)\left|a\right\rangle dt'\\\\\
 & -\int\_{0}^{t}dt'\int\_{0}^{t'}dt^{\prime\prime}\left\langle a\right|\hat{V}\_{I}(t')\hat{V}\_{I}(t'')\left\|a\right\rangle \\\\\
 & +\cdots
\end{split}
\end{align}

The expectation value in the first integral is

\begin{equation}
\left\langle a\right\|\hat{V}\_{I}(t)\left\|a\right\rangle = 0.
\end{equation}

To calculate the expectation value in the second integral, the operator product $\hat{V}\_{I}(t')\hat{V}\_{I}(t'')$ is worked out.

\begin{align}
\begin{split}
&\hat{V}\_{I}(t')\hat{V}\_{I}(t'') \\\\\
= & g_{ab}^{2}e^{i\hat{h}\_{a}t'}e^{-i\hat{h}\_{b}(t'-t'')}e^{-i\hat{h}\_{a}t}\left\|a\right\rangle \left\langle a\right\| +\\\\\
& g\_{ac}^{2}e^{i\hat{h}\_{a}t}e^{-i\hat{h}\_{c}(t'-t'')}e^{-i\hat{h}\_{a}t}\left\|a\right\rangle \left\langle a\right\| + \\\\\
 & \mathrm{something}\left\|b\right\rangle \left\langle b\right\| +\mathrm{something}\left\|c\right\rangle \left\langle c\right\|\\
\end{split}
\end{align}

Thus, the expectation integral is

\begin{equation}
\int\_{0}^{t}dt'\int\_{0}^{t'}dt^{\prime\prime}\left(g\_{ab}^{2}e^{i\hat{h}\_{a}t'}e^{-i\hat{h}\_{b}(t'-t'')}e^{-i\hat{h}\_{a}t}+g\_{ac}^{2}e^{i\hat{h}\_{a}t}e^{-i\hat{h}\_{c}(t'-t'')}e^{-i\hat{h}\_{a}t}\right)
\end{equation}

Each term in the integral is identical to a 2-state expression (i.e. when the third state doesn't exist).



# References

[1] Coalson, R. D., Evans, D. G., & Nitzan, A. (1994). A nonequilibrium golden rule formula for electronic state populations in nonadiabatically coupled systems. [The Journal of chemical physics, 101(1), 436-448](https://aip.scitation.org/doi/pdf/10.1063/1.468153?casa_token=RaVT3yAPjcYAAAAA:EvvhZi0bMPj5J1uw4YRzZI2Cv2TXpXPJ3pxhWCqlVs8L0lTgiBxXuJ37Vnno_GiYapzEuvNVVbMz).