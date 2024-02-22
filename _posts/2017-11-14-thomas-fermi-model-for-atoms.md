---
layout: post
title: Thomas-Fermi Model for Atoms
category: Science
tags: [Fermi gas, Electron]
img: "2017-11-14-thomas-fermi-model-for-atoms.png"
strip: "2017-11-14-thomas-fermi-model-for-atoms-strip.png"
tex: true
author: Linus
source:
  title: 硬核化学物理HCChemPhysics
  url: https://mp.weixin.qq.com/s?__biz=MzUxMDQ4MDMwNw==&mid=2247483654&idx=1&sn=cb339abecd87c777e19d705981b003d4&chksm=f9031bdace7492ccdf69986654765ead690ff8ea90c316fd4bdea9ab59d8be9d87b1fba98b26&mpshare=1&scene=1&srcid=1114nnV0kMKZWWVtPJB4UAPn&pass_ticket=XI44z0m8bcWi2cCd%2B74OJcNdHIzFyvnnR7%2BXunGjO1DUriT0Pgq9hE6Xx%2BCscJF4##
---

## From Bound States to Plan Waves (*from finite to infinite*)
By pushing the bound environment to the infinity, we could get the behaviour of the system at $\infty$. For a non-potential system with periodic boundary condition, the wfn is:

$$
\varphi_{n}=\frac{1}{\sqrt{L}}\exp(ik_{n}z),\quad k_{n}=\frac{2\pi}{L}n,\quad n\in\mathbb{Z}
$$

and the energy corresponding to the state is $\varepsilon_{n}=\frac{\hbar^{2}}{2m}k_{n}^{2}$ with a certain momentum$\vec{p}=\hbar k$.

A time-dependent version of the wfn of free particles could be derived from Schrodinger equation by the method of sepration of variables, while the independent version is the direct result of a homogeneous linear differential equation.

Let's move to the free electron gas model now where the wfn above would be utilized. Consider the $k$-space, where all $k$ vectors are dispered homogeneously, which means that for every small volume $\Delta k=\frac{(2\pi)^{3}}{V}$, the number of states in it is only pure $2$, taking spin states into consideration. Furthermore, for a system at ground state by which we mean that all of the states below the highest one are occupied, where the highest energy the electron posesses is

$$
\varepsilon_{n_{F}}=\frac{\hbar^{2}}{2m}k_{F}^{2},
$$

the number of states is

$$
2\cdot\frac{4}{3}\pi k_{F}^{3}/\left(\frac{(2\pi)^{3}}{V}\right)=\frac{1}{3\pi^{2}}\left(k_{F}\right)^{3}/V=\rho\cdot V,
$$

thus $\rho=\frac{1}{3\pi^{2}}\left(k_{F}\right)^{3}$ or say $\rho=\frac{1}{3\pi^{2}}\left(p_{F}/\hbar\right)^{3}$. At this point we get the density of the electrons in a homogeneous system in terms of the hightest momentum, besides, we could express the formula in terms of highest energy whcih is not short of any information.

Now let's consider a single atom. Though atoms are not a bit similar as the homogeneous electron gas at the first glance, we could have a try. If somewhere the density of electrons are homogeneous, then the ground state of this area is such that the states below and on the Fermi momentum surface are all occupied. So if somwhere the density changes very slowly, we could regrad it as HEG and give out the density of electrons at this point, to the extent of differential element, in terms of the highest energy of electrons at the volume. For every differential element, in which we could select a certain point $x$, the relation between the Fermi momentum and DOS is:

$$
\rho(x)=\frac{1}{3\pi^{2}}\left(\frac{p_{F}(x)}{\hbar}\right).
$$

and the DOE $\times$ the differential volume $=\epsilon_{k}(x)\Delta V$ is

$$
\epsilon_{k}(x)\Delta V=2\cdot\int_{0}^{k_{F}}\frac{\hbar^{2}k^{2}}{2m}4\pi k^{2}\frac{\text{d}k}{\Delta k=\frac{(2\pi)^{3}}{\Delta V}},
$$

thus

$$
\epsilon_{k}=\int_{0}^{k_{F}}\frac{2\hbar^{2}k^{2}}{m\pi^{2}}k^{2}\text{d}k=\frac{1}{10}k_{F}^{5}\hbar^{2}/m\pi^{2}=\frac{3}{10m}p_{F}(x)\rho(x)\\=\frac{3\hbar^{2}}{10m}(3\pi^{2})^{2/3}\rho^{5/3}(x)
$$

Now let's consider a small volume in a potential field $V(x)=\phi(x)$. For a system at equilibrim, we could forsee the the highest energy of any small volume must be indential, otherwise the electrons would flow into the volume with lower energy. By this assertion we know:

$$
\frac{\hbar^{2}}{2m}p_{F}^{2}(x)-e\phi(x)=\frac{\hbar^{2}}{2m}(3\pi^{2})^{2/3}[\rho(x)]^{2/3}=\text{const}
$$

At another point, the density of electrons is related to the potential by Possion equation $\Delta\phi(x)=4\pi e\rho(x)$. If we set the potential at infinity $\phi_{0}(\infty)=0$, then the $\text{const}=0$. For the information of $\rho(x)$, we must solve Possion equation:

$$
\Delta\phi(x)=e(2me)^{3/2}\left(\frac{1}{3\pi^{2}\hbar^{3}}\right)\phi(x)
$$

If the potential $\phi$ is spherically symmetric, the we could take a transformation:

$$
\phi(x)=\frac{ze}{|\vec{x}|}\chi(\xi),\quad\xi=\frac{2m^{2}}{\hbar^{2}}z^{1/3}|\vec{x}|
$$

where $z$ is the atomic number of the atom.

Finally we get

$$
\xi^{\frac{1}{2}}\chi''(\xi)=\frac{4\pi}{3}[\chi(\xi)]^{3/2}
$$

which is the Thomas-Fermi equation.

Additionally, if there existing some angular momentum for the electrons, we must add corresponding terms into the form of potential funtion$V(x).$ About this kind of addtion, one may refer to the Quantum
Mechancs: Special Topics by Walter Greiner.

> ![#33b5e5](https://placehold.it/15/33b5e5/000000?text=+)Note:  
> A note for the transformation above and the solving method of Thomas-Fermi equation:  
Fot $r$ or say $|\vec{x}|\to0$, we may require $\phi(r)\to Ze/r$, that may be the reason why we transform in this way. Of course if the $\phi$ is only the funtion of $|\vec{r}|$, from

> $$
\Delta\phi(r)=\frac{1}{r^{2}}\frac{\partial}{\partial r}r^{2}\frac{\partial}{\partial r}\phi(r)=\frac{1}{r^{2}}[2r\phi'(r)+r^{2}\phi''(r)]\\=\phi''(r)+\frac{2}{r}\phi'(r)=\frac{1}{r}\frac{\partial^{2}}{\partial r^{2}}(r\phi(r))
$$

最后插几句，Thomas Fermi方程所谓的$x$尺度不变方程，我们可以做一个代换: $y\to x^{-3}u(x)$ ，变为一个自洽方程，此时就可以用self-consistent + Rayleigh-Ritz 变分的办法来求解，关于尺度不变方程和自洽方程之间的关系，可以参考Carl Bender（本德）的高等应用数学方法（中译本）一书，英文名：*Advanced Mathematical Methods for Scientists and Engineers*.

## References
1. 汤川秀树          量子力学
2. Walter Greiner 量子力学
3. 本德                  高等应用数学方法