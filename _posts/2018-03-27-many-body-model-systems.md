---
layout: post
title: 多体模型系统
category: Science
tags: [Second quantisation, Quantum mechanics]
img: "2018-03-27-many-body-model-systems.png"
strip: "2018-03-27-many-body-model-systems-strip.png"
tex: true
toc: true
---

本文介绍几个理论固体物理常用的模型系统，并对其要素进行论证和检验。在构造模型哈密顿量时，可实践[二次量子化]({{ site.url }}/second-quantisation)。

固体当然是多体系统，

$$
\text{Solid}=\sum_{i=1}^{N}\text{(particles)}_i
$$

由相互作用的原子或分子构成。每个*粒子*由一个或多个带正电的原子核和一个带负电的电子云组成。电子云可分为**核心电子**(core electrons)和**价电子**(valence electrons)（[图 1](#fig-1)）。核心电子紧紧束缚在原子核周围，通常占据封闭电子层——例外如稀土元素的$4f$层电子——对固体特性几乎没什么影响。价电子恰恰相反，它们占据非封闭壳层并负责成键构成固体。当然，核心电子和价电子之间的并非总是界限分明，这已是一种近似处理。在此意义上，**晶格离子**(lattice ion)指的是原子核与核心电子的结合体。由此得到以下模型:

> **固体**：  
> 一个由晶格离子和价电子组成的相互作用粒子系统。

<figure id="fig-1">
  <img src="{{ '2018-03-27-many-body-model-systems-drude-model.png' | prepend:'/upload/posts/' | relative_url }}" alt="Drude Model">
  <figcaption><b>图 1</b> (a)孤立原子示意图（未按比例画）。(b)离子及价电子示意图。</figcaption>
</figure>

相应的哈密顿量为：

\begin{equation}
\label{eq:1}
H=H\_{\text{e}}+H\_{\text{i}}+H\_{\text{ei}}
\end{equation}

**电子子系统**由算符$H\_{\text{e}}$描述：

\begin{equation}
\label{eq:2}
H\_{\text{e}}=\sum\_{i=1}^{N\_\text{e}}\frac{p\_i^2}{2m}+\frac{1}{2}\frac{1}{4\pi\varepsilon\_0}\sum\_{i,j}^{i\neq j}\frac{e^2}{|\boldsymbol{r}\_i-\boldsymbol{r}\_j|}\equiv H\_\text{e,kin}+H\_\text{ee}
\end{equation}

$N\_\text{e}$是价电子数目。上式第一项表示动能，第二项是库伦相互作用。$\boldsymbol{r}\_i$，$\boldsymbol{r}\_j$是电子位置矢量。

**离子子系统**由算符$H\_{\text{i}}$描述：

\begin{equation}
\label{eq:3}
H\_{\text{i}}=\sum\_{\alpha=1}^{N\_\text{i}}\frac{p\_\alpha^2}{2M\_\alpha}+\frac{1}{2}\sum\_{\alpha,\beta}^{\alpha\neq \beta}V\_\text{i}(\boldsymbol{R}\_\alpha-\boldsymbol{R}\_\beta)\equiv H\_\text{i,kin}+H\_\text{ii}
\end{equation}

离子-离子相互作用现在还不必明确写出，它总是成对作用，并对离子的平衡位置，$\boldsymbol{R}\_\alpha^{(0)}$，构成严格的周期性晶格有所贡献。离子在平衡位置振荡，振荡能量是量子化的，基本量子叫做声子。方便起见，将$H\_\text{ii}$分成：

\begin{equation}
\label{eq:4}
H\_\text{ii}=H\_\text{ii}^{(0)}+H\_\text{p}
\end{equation}

$H\_\text{ii}^{(0)}$决定了固体的一些特性，例如固体中成键，而$H\_\text{p}$则属于晶格动力学。

最后，**两子系统间的相互作用**是

\begin{equation}
\label{eq:5}
H\_\text{ei}=\sum\_{i=1}^{N\_\text{e}}\sum\_{\alpha=1}^{N\_\text{i}}V\_\text{ei}(\boldsymbol{r}\_i-\boldsymbol{R}\_\alpha)
\end{equation}

方便起见，这里也做进一步分解：

\begin{equation}
\label{eq:6}
H\_\text{ei}=H\_\text{ei}^{(0)}+H\_\text{e-p}
\end{equation}

$H\_\text{ei}^{(0)}$表示电子与处于平衡位置的离子间的相互作用而$H\_\text{e-p}$表示电子-声子相互作用。

得到整个系统\eqref{eq:1}的精确解几乎不可能。可由以下三个步骤做个近似：
1. 电子运动项，例如，在一个刚性的离子晶格中：$H\_\text{e}+H\_\text{ei}^{(0)}$。
2. 离子运动项，例如，在均匀的电子气中：$H\_\text{p}$。
3. 耦合项，例如，用微扰理论处理：$H\_\text{e-p}$。

接下来根据以上概念讨论电子子系统。

## 1 晶体电子
### 1.1 无相互作用Bloch电子
首先考虑刚性离子晶格中的电子，它们之间无相互作用，仅仅受周期性的晶格势影响，即如下哈密顿量：

\begin{equation}
\label{eq:7}
H\_0=H\_\text{e,kin}+H\_\text{ei}^{(0)}
\end{equation}

**晶格势**(lattice potential)来自处于平衡位置的离子：

\begin{equation}
\label{eq:8}
\widehat{V}(\boldsymbol{r}\_i)=\sum\_{\alpha=1}^{N\_\text{i}}V\_\text{ei}(\boldsymbol{r}\_i-\boldsymbol{R}\_\alpha^{(0)})
\end{equation}

更准确地说，离子的位置$\boldsymbol{R}\_\alpha^{(0)}$为：

\begin{equation}
\label{eq:9}
\begin{split}
\boldsymbol{R}\_\alpha^{(0)}\Rightarrow\boldsymbol{R}\_s^\boldsymbol{n}=\boldsymbol{R}^\boldsymbol{n}+\boldsymbol{R}\_s\\\
\boldsymbol{n}=(n\_1,n\_2,n\_3);\quad n\_i\in\mathbb{Z}
\end{split}
\end{equation}

这里的$\boldsymbol{R}\_s^\boldsymbol{n}$是Bravais格子：

\begin{equation}
\label{eq:10}
\boldsymbol{R}^\boldsymbol{n}=\sum\_{i=1}^{3}n\_i\boldsymbol{a}\_i
\end{equation}

$\boldsymbol{a}\_1$，$\boldsymbol{a}\_2$，$\boldsymbol{a}\_3$是初基平移矢量，$\boldsymbol{R}\_s$是初基原子的位置矢量。Bravais格子的周期性体现在：

\begin{equation}
\label{eq:11}
\widehat{V}(\boldsymbol{r}\_i+\boldsymbol{R}^\boldsymbol{n})\overset{!}{=}\widehat{V}(\boldsymbol{r}\_i)
\end{equation}

$\widehat{V}(\boldsymbol{r}\_i)=\widehat{V}(\hat{\boldsymbol{r}}\_i)$是单粒子算符，可以代入

\begin{equation}
\label{eq:12}
H\_\text{ei}^{(0)}=\sum\_{i=1}^{N\_\text{e}}\widehat{V}(\hat{\boldsymbol{r}}\_i)
\end{equation}

解如下本征值方程：

\begin{equation}
\label{eq:13}
h\_0\psi\_\boldsymbol{k}(\boldsymbol{r})=\varepsilon(\boldsymbol{k})\psi\_\boldsymbol{k}(\boldsymbol{r})
\end{equation}

称$\psi\_\boldsymbol{k}(\boldsymbol{r})$为**Bloch函数**而$\varepsilon(\boldsymbol{k})$为相应**Bloch能**。$\boldsymbol{k}$是第一布里渊区中的波矢，$h\_0$表示算符：

\begin{equation}
\label{eq:14}
h\_0=\frac{\boldsymbol{p}^2}{2m}+\widehat{V}(\hat{\boldsymbol{r}})
\end{equation}

方程\eqref{eq:13}的解并不简单。利用周期性条件\eqref{eq:11}可以导出基本的**Bloch定理**：

\begin{equation}
\label{eq:15}
\psi\_\boldsymbol{k}(\boldsymbol{r}+\boldsymbol{R}^\boldsymbol{n})=e^{i\boldsymbol{k}\cdot\boldsymbol{R}^\boldsymbol{n}}\psi\_\boldsymbol{k}(\boldsymbol{r})
\end{equation}

通常记作：

\begin{equation}
\label{eq:16}
\psi\_\boldsymbol{k}(\boldsymbol{r})=u\_\boldsymbol{k}(\boldsymbol{r})e^{i\boldsymbol{k}\cdot\boldsymbol{r}}
\end{equation}

振幅函数必须满足Bravais格子的周期性：

\begin{equation}
\label{eq:17}
u\_\boldsymbol{k}(\boldsymbol{r}+\boldsymbol{R}^\boldsymbol{n})=u\_\boldsymbol{k}(\boldsymbol{r})
\end{equation}

Bloch函数$\psi\_\boldsymbol{k}(\boldsymbol{r})$是正交完备的：

\begin{align}
\label{eq:18}
\int\mathrm{d}^3r\psi\_\boldsymbol{k}^\*(\boldsymbol{r})\psi\_\boldsymbol{k'}(\boldsymbol{r})&=\delta\_{\boldsymbol{k},\boldsymbol{k}'}\\\
\label{eq:19}
\sum\_\boldsymbol{k}^{\text{1.BZ}}\psi\_\boldsymbol{k}^\*(\boldsymbol{r})\psi\_\boldsymbol{k}(\boldsymbol{r}')&=\delta(\boldsymbol{r}-\boldsymbol{r}')
\end{align}

求和历遍第一布里渊区中的所有波矢$\boldsymbol{k}$，由于周期性边界条件，它们是离散的。$h\_0$中不包含自旋部分，故其本征函数可分解为自旋和位形空间的函数：

\begin{align}
\label{eq:20}
\begin{split}
|\boldsymbol{k}\sigma\rangle &\Longleftrightarrow \text{Bloch state}\\\
\langle\boldsymbol{r}|\boldsymbol{k}\sigma\rangle&=\psi\_{\boldsymbol{k}\sigma}(\boldsymbol{r})=\psi\_\boldsymbol{k}(\boldsymbol{r})\chi\_\sigma\\\
\chi\_\uparrow&=\begin{pmatrix}1\\\0\end{pmatrix};\quad\chi\_\downarrow=\begin{pmatrix}0\\\1\end{pmatrix}
\end{split}
\end{align}

如果考虑来自不同能带的电子，Bloch函数将带有能带指标$n$。现在不考虑这些，下面的讨论仅限处于同一能带的电子。

定义：

$$
a_{\boldsymbol{k}\sigma}^\dagger(a_{\boldsymbol{k}\sigma}):\quad\text{Bloch电子的产生（湮灭）算符}
$$

$H\_0$是单体算符，由[式(214)-二次量子化](/blog/second-quantisation#mjx-eqn-eq214)可得：

$$
H_0=\sum_{\substack{\boldsymbol{k}\sigma\\\boldsymbol{k}'\sigma'}}\langle\boldsymbol{k}\sigma|h_0|\boldsymbol{k}'\sigma'\rangle a_{\boldsymbol{k}\sigma}^\dagger a_{\boldsymbol{k}'\sigma'}
$$

矩阵元可直接计算得到：

\begin{equation}
\label{eq:21}
\langle\boldsymbol{k}\sigma|h\_0|\boldsymbol{k}'\sigma'\rangle=\varepsilon(\boldsymbol{k}')\langle\boldsymbol{k}\sigma|\boldsymbol{k}'\sigma'\rangle=\varepsilon(\boldsymbol{k})\delta\_{\boldsymbol{kk'}}\delta\_{\sigma\sigma'}
\end{equation}

上式中$\|\boldsymbol{k}\sigma\rangle$是$h\_0$本征函数。由此得到：

\begin{equation}
\label{eq:22}
H\_0=\sum\_{\boldsymbol{k}\sigma}\varepsilon(\boldsymbol{k})a\_{\boldsymbol{k}\sigma}^\dagger a\_{\boldsymbol{k}\sigma}=\sum\_{\boldsymbol{k}\sigma}\varepsilon(\boldsymbol{k})n\_{\boldsymbol{k}\sigma}
\end{equation}

*Bloch算符*$a\_{\boldsymbol{k}\sigma}$，$a\_{\boldsymbol{k}\sigma}^\dagger$自然满足基本对易关系：

\begin{align}
\label{eq:23}
[a\_{\boldsymbol{k}\sigma},a\_{\boldsymbol{k}'\sigma'}]\_+&=[a\_{\boldsymbol{k}\sigma}^\dagger,a\_{\boldsymbol{k}'\sigma'}^\dagger]\_+=0\\\
\label{eq:24}
[a\_{\boldsymbol{k}\sigma},a\_{\boldsymbol{k}'\sigma'}^\dagger]\_+&=\delta\_{\boldsymbol{kk'}}\delta\_{\sigma\sigma'}
\end{align}

如果忽略固体晶格结构而将离子晶格视作正电荷背景($\widehat{V}(\boldsymbol{r})=\text{const}$)，Bloch函数将成为平面波，

\begin{equation}
\label{eq:25}
\psi\_\boldsymbol{k}(\boldsymbol{r})\underset{[\widehat{V}(\boldsymbol{r})=\text{const}]}{\Rightarrow}\frac{1}{\sqrt{V}}e^{i\boldsymbol{k}\cdot\boldsymbol{r}}
\end{equation}

相应Bloch能，由$p^2/2m=-(\hbar^2/2m)\Delta$：

\begin{equation}
\label{eq:26}
\varepsilon(\boldsymbol{k})\underset{[\widehat{V}(\boldsymbol{r})=\text{const}]}{\Rightarrow}\frac{\hbar^2k^2}{2m}
\end{equation}

（这里$V$是固体的体积，要注意区分$V$和晶格势$\widehat{V}$！）接着讨论两种颇具应用性的两种其他表象，比如

> **场算符**(field operators):
> 
> $$
\widehat{\psi}\_\sigma^\dagger(\boldsymbol{r}),\widehat{\psi}\_\sigma(\boldsymbol{r})
$$

可由[式(165)—式(175)-二次量子化](//mageluer.coding.me/blog/second-quantisation#mjx-eqn-eq165)进行理解，只不过加入了电子自旋，其对易关系也可按[二次量子化](//mageluer.coding.me/blog/second-quantisation)中进行推广，例如：

\begin{equation}
\label{eq:27}
[\widehat{\psi}\_\sigma(\boldsymbol{r}),\widehat{\psi}\_{\sigma'}^\dagger(\boldsymbol{r}')]\_+=\delta(\boldsymbol{r}-\boldsymbol{r}')\delta\_{\sigma\sigma'}
\end{equation}

由此得到$H\_0$：

\begin{align}
\label{eq:28}
\begin{split}
H\_0&=\sum\_{\sigma,\sigma'}\iint\mathrm{d}^3r\,\mathrm{d}^3r'\langle\boldsymbol{r}\sigma|h\_0|\boldsymbol{r}'\sigma'\rangle\widehat{\psi}\_\sigma^\dagger(\boldsymbol{r})\widehat{\psi}\_{\sigma'}(\boldsymbol{r}')=\\\
&=\sum\_{\sigma,\sigma'}\iint\mathrm{d}^3r\,\mathrm{d}^3r'\delta\_{\sigma\sigma'}\left(-\frac{\hbar^2}{2m}\Delta\_{\boldsymbol{r}'}+\widehat{V}(\boldsymbol{r}')\right)\delta(\boldsymbol{r}-\boldsymbol{r}')\widehat{\psi}\_\sigma^\dagger(\boldsymbol{r})\widehat{\psi}\_{\sigma'}(\boldsymbol{r}')=\\\
&=\sum\_{\sigma}\int\mathrm{d}^3r\widehat{\psi}\_\sigma^\dagger(\boldsymbol{r})\left(-\frac{\hbar^2}{2m}\Delta\_{\boldsymbol{r}}+\widehat{V}(\boldsymbol{r})\right)\widehat{\psi}\_\sigma(\boldsymbol{r})
\end{split}
\end{align}

此外，一个常用的特殊表象利用了

> **Wannier函数**：  
> \begin{equation}
\label{eq:29}
\omega(\boldsymbol{r}-\boldsymbol{R}\_i)=\frac{1}{\sqrt{N\_\text{i}}}\sum\_{\boldsymbol{k}}^{\text{1.BZ}}e^{-i\boldsymbol{k}\cdot\boldsymbol{R}\_i}\psi\_{\boldsymbol{k}\sigma}(\boldsymbol{r})
\end{equation}

<figure id="fig-2">
  <img src="{{ '2018-03-27-many-body-model-systems-wannier-function.png' | prepend:'/upload/posts/' | relative_url }}" alt="Wannier function">
  <figcaption><b>图 2</b> 定性的Wannier函数实部对位置的依赖性。</figcaption>
</figure>

此函数的一个典型特征是在格点$R\_\text{i}$处高度局域化（[图 2](#fig-2)）。由式\eqref{eq:18}及

\begin{equation}
\label{eq:30}
\frac{1}{N\_\text{i}}\sum\_{\boldsymbol{k}}^{\text{1.BZ}}e^{-i\boldsymbol{k}\cdot(\boldsymbol{R}\_i-\boldsymbol{R}\_j)}=\delta\_{ij}
\end{equation}

可以证明其正交关系：

\begin{equation}
\label{eq:31}
\int\mathrm{d}^3r\omega\_\sigma^\*(\boldsymbol{r}-\boldsymbol{R}\_i)\omega\_\sigma^\*(\boldsymbol{r}-\boldsymbol{R}\_j)=\delta\_{\sigma\sigma'}\delta\_{ij}
\end{equation}

采用如下记号：

\begin{align}
\label{eq:32}
\begin{split}
|i\sigma\rangle&\Longleftrightarrow\text{Wannier state}\\\
\langle\boldsymbol{r}|i\sigma\rangle&=\omega\_\sigma(\boldsymbol{r}-\boldsymbol{R\_i})\\\
a\_{i\sigma}^\dagger(a\_{i\sigma}):&\text{格矢}\boldsymbol{R}\_i\text{处电子Wannier态的产生（湮灭）算符}
\end{split}
\end{align}

$H\_0$的二次量子化形式为：

\begin{equation}
\label{eq:33}
H\_0=\sum\_{ij\sigma}T\_{ij}a\_{i\sigma}^\dagger a\_{j\sigma}
\end{equation}

其物理图像相当清晰：处于$\boldsymbol{R}\_j$处（于此湮灭）自旋为$\sigma$的电子*跃迁*到格点$\boldsymbol{R}\_i$（于此产生）。故$T\_{ij}$被称作

<p style="text-align: center"><b>"跃迁"积分</b></p>

下面开始具体计算：

\begin{align}
\begin{split}
\langle i\sigma|h\_0|j\sigma'\rangle&=\delta\_{\sigma\sigma'}\langle i\sigma|h\_0|j\sigma\rangle=\\\
&=\delta\_{\sigma\sigma'}\sum\_{\substack{\boldsymbol{k},\boldsymbol{k}'\\\
\sigma\_1,\sigma\_2}}\langle i\sigma|\boldsymbol{k}\sigma\_1\rangle\langle\boldsymbol{k}\sigma\_1|h\_0|\boldsymbol{k}'\sigma\_2\rangle\langle\boldsymbol{k}'\sigma\_2|j\sigma\rangle=\\\
&=\delta\_{\sigma\sigma'}\sum\_{\substack{\boldsymbol{k},\boldsymbol{k}'\\\
\sigma\_1,\sigma\_2}}\varepsilon(\boldsymbol{k}')\langle i\sigma|\boldsymbol{k}\sigma\_1\rangle\langle\boldsymbol{k}\sigma\_1|\boldsymbol{k}'\sigma\_2\rangle\langle\boldsymbol{k}'\sigma\_2|j\sigma\rangle=\\\
&=\delta\_{\sigma\sigma'}\sum\_{\boldsymbol{k},\sigma\_1}\varepsilon(\boldsymbol{k})\langle i\sigma|\boldsymbol{k}\sigma\_1\rangle\langle\boldsymbol{k}\sigma\_1|j\sigma\rangle
\end{split}
\label{eq:34}
\end{align}

剩余矩阵元作如下计算：

\begin{align}
\label{eq:35}
\begin{split}
\langle i\sigma|\boldsymbol{k}\sigma\_1\rangle&=\int\mathrm{d}^3\langle i\sigma|\boldsymbol{r}\rangle\langle\boldsymbol{r}|\boldsymbol{k}\sigma\_1\rangle=\\\
&=\int\mathrm{d}^3\omega\_\sigma^\*(\boldsymbol{r}-\boldsymbol{R}\_i)\psi\_{\boldsymbol{k}\sigma\_1}(\boldsymbol{r})=\\\
&=\frac{1}{\sqrt{N\_\text{i}}}\sum\_{\boldsymbol{k}'}e^{i\boldsymbol{k}\cdot\boldsymbol{R}\_i}\int\mathrm{d}^3r\psi\_{\boldsymbol{k}'\sigma}^\*(\boldsymbol{r})\psi\_{\boldsymbol{k}\sigma\_1}(\boldsymbol{r})=\\\
&=\frac{1}{\sqrt{N\_\text{i}}}\sum\_{\boldsymbol{k}'}e^{i\boldsymbol{k}\cdot\boldsymbol{R}\_i}\delta\_{\boldsymbol{kk}'}\delta\_{\sigma\sigma\_1}=\delta\_{\sigma\sigma\_1}\frac{e^{i\boldsymbol{k}\cdot\boldsymbol{R}\_i}}{\sqrt{N\_\text{i}}}
\end{split}
\end{align}

上式第三行用到式\eqref{eq:29}，由此得到式\eqref{eq:34}：

\begin{equation}
\label{eq:36}
\langle i\sigma|h\_0|j\sigma'\rangle=\delta\_{\sigma\sigma'}T\_{ij}
\end{equation}

相应的：

\begin{equation}
\label{eq:37}
T\_{ij}=\sum\_{\boldsymbol{k},\sigma\_1}\varepsilon(\boldsymbol{k})\delta\_{\sigma\sigma\_1}\frac{e^{i\boldsymbol{k}\cdot\boldsymbol{R}\_i}}{\sqrt{N\_\text{i}}}\delta\_{\sigma\sigma\_1}\frac{e^{-i\boldsymbol{k}\cdot\boldsymbol{R}\_j}}{\sqrt{N\_\text{i}}}=\frac{1}{N\_\text{i}}\sum\_\boldsymbol{k}\varepsilon(\boldsymbol{k})e^{i\boldsymbol{k}\cdot(\boldsymbol{R}\_i-\boldsymbol{R}\_j)}
\end{equation}

其逆为：

\begin{equation}
\label{eq:38}
\varepsilon(\boldsymbol{k})=\frac{1}{N\_\text{i}}\sum\_{i,j}T\_{ij}e^{-i\boldsymbol{k}\cdot(\boldsymbol{R}\_i-\boldsymbol{R}\_j)}
\end{equation}

代入式\eqref{eq:37}再结合式\eqref{eq:30}易验证：

\\[
\begin{split}
&\frac{1}{N\_\text{i}}\sum\_\boldsymbol{k}\varepsilon(\boldsymbol{k})e^{i\boldsymbol{k}\cdot(\boldsymbol{R}\_i-\boldsymbol{R}\_j)}=\\\
=&\frac{1}{N\_\text{i}}\sum\_\boldsymbol{k}\left(\frac{1}{N\_\text{i}}\sum\_{i',j'}T\_{i'j'}e^{-i\boldsymbol{k}\cdot(\boldsymbol{R}\_{i'}-\boldsymbol{R}\_{j'})}\right)e^{i\boldsymbol{k}\cdot(\boldsymbol{R}\_i-\boldsymbol{R}\_j)}=\\\
=&\sum\_{i',j'}T\_{i'j'}\sum\_\boldsymbol{k}\left(\frac{1}{N\_\text{i}}e^{i\boldsymbol{k}\cdot(\boldsymbol{R}\_{i}-\boldsymbol{R}\_{i'})}\right)\left(\frac{1}{N\_\text{i}}e^{i\boldsymbol{k}\cdot(\boldsymbol{R}\_{j'}-\boldsymbol{R}\_{j})}\right)=\\\
=&\sum\_{i',j'}T\_{i'j'}\delta\_{ii'}\delta\_{jj'}=\\\
=&T\_{ij}
\end{split}
\\]

Bloch算符和Wannier算符之间的关系可仿照[式(171)-二次量子化](https://mageluer.coding.me/blog/second-quantisation#mjx-eqn-eq172)得到：

\begin{align}
\label{eq:39}
a\_{i\sigma}=\frac{1}{\sqrt{N\_\text{i}}}\sum\_{\boldsymbol{k}}^{\text{1.BZ}}e^{i\boldsymbol{k}\cdot\boldsymbol{R}\_i}a\_{\boldsymbol{k}\sigma}\\\
a\_{\boldsymbol{k}\sigma}=\frac{1}{\sqrt{N\_\text{i}}}\sum\_{i=1}^{N\_\text{i}}e^{-i\boldsymbol{k}\cdot\boldsymbol{R}\_i}a\_{i\sigma}\\\
\end{align}

由Bloch算符的对易关系\eqref{eq:23}，\eqref{eq:24}可得到Wannier算符的对易关系：
\begin{align}
\label{eq:41}
[a\_{i\sigma},a\_{j\sigma'}]\_+&=[a\_{i\sigma}^\dagger,a\_{j\sigma'}^\dagger]\_+=0\\\
\label{eq:42}
[a\_{i\sigma},a\_{j\sigma'}^\dagger]\_+&=\delta\_{ij}\delta\_{\sigma\sigma'}
\end{align}

### 1.2 凝胶模型
此模型足以描述简单金属，且基于如下假设：

1. 处于体积$V=L^3$中的$N\_\text{e}$个电子之间为库伦相互作用：  
\begin{equation}
\label{eq:43}
H\_\text{ee}=\frac{e^2}{8\pi\varepsilon\_0}\sum\_{i,j}^{i\neq j}\frac{1}{|\boldsymbol{r}\_i-\boldsymbol{r}\_j|}
\end{equation}
2. 离子仅带一个正电荷：  
\begin{equation}
\label{eq:44}
N\_\text{e}=N\_\text{i}=N
\end{equation}
3. 离子形成均匀的背景场并保证：(a)体系电荷中性；(b)晶格势为常值。  
此时Bloch函数为平面波形式：  
\begin{equation}
\label{eq:45}
\psi\_{\boldsymbol{k}\sigma}(\boldsymbol{r})\Rightarrow\frac{1}{\sqrt{V}}e^{i\boldsymbol{k}\cdot\boldsymbol{r}}\chi\_\sigma
\end{equation}
4. 周期性边界条件导致波矢离散化：  
\begin{equation}
\label{eq:46}
\boldsymbol{k}=\frac{2\pi}{L}(n\_x,n\_y,n\_z),\quad n\_{x,y,z}\in\boldsymbol{Z}
\end{equation}

符合这些假设的模型哈密顿的一次量子化形式是什么样？它应包含如下三项：

\begin{equation}
\label{eq:47}
H=H\_\text{e}+H\_++H\_\text{e+}
\end{equation}

$H\_\text{e}$是关键项，其意义见式\eqref{eq:2}。$H\_+$表示均匀分布的离子电荷，*均匀分布*的意思是离子的电荷密度$n(\boldsymbol{r})$与位置无关：

\begin{equation}
\label{eq:48}
n(\boldsymbol{r})\Rightarrow\frac{N}{V}
\end{equation}

$H\_+$项为：
\begin{equation}
\label{eq:49}
H\_+=\frac{e^2}{8\pi\varepsilon\_0}\iint\mathrm{d}^3r\,\mathrm{d}^3r'\frac{n(\boldsymbol{r})\cdot n(\boldsymbol{r'})}{|\boldsymbol{r}-\boldsymbol{r'}|}e^{-\alpha|\boldsymbol{r}-\boldsymbol{r'}|}
\end{equation}

基于第4个假设，我们的结果应在热力学极限下讨论，即$N\to\infty,V\to\infty,N/V\to\text{const}$。由于库仑力长程有效，积分会发散，于是加上一个收敛因子$\exp(-\alpha\|\boldsymbol{r}-\boldsymbol{r'}\|)$，$\alpha>0$。积分完成后再令$\alpha\to0$。

结合\eqref{eq:48}可得：

\\[
\begin{split}
&\iint\mathrm{d}^3r\,\mathrm{d}^3r'\frac{e^{-\alpha|\boldsymbol{r}-\boldsymbol{r'}|}}{|\boldsymbol{r}-\boldsymbol{r'}|}=\\\
=&\iint\mathrm{d}^3r\,\mathrm{d}^3r'\frac{e^{-\alpha r}}{r}=\qquad(\boldsymbol{r}-\boldsymbol{r'}\to\boldsymbol{r},\boldsymbol{r'}\to\boldsymbol{r'})\\\
=&V\int_V\mathrm{d}^3r\frac{e^{-\alpha r}}{r}=\\\
=&V\int_0^\infty\mathrm{d}r4\pi re^{-\alpha r}=\\\
=&\frac{4\pi V}{\alpha^2}
\end{split}
\\]

上式用到了：

\\[
\begin{split}
&\int_0^\infty\mathrm{d}x\,\, x^ne^{-\alpha x}=\\\
=&\int_0^\infty\mathrm{d}x\,\,(-1)^n\frac{\mathrm{d}^n}{\mathrm{d}\alpha^n}e^{-\alpha x}=\\\
=&(-1)^n\frac{\mathrm{d}^n}{\mathrm{d}\alpha^n}\int_0^\infty\mathrm{d}x\,\, e^{-\alpha x}=\\\
=&(-1)^n\frac{\mathrm{d}^n}{\mathrm{d}\alpha^n}\frac{1}{\alpha}=\\\
=&(-1)^n\frac{(-1)^n}{\alpha^{n+1}}=\\\
=&\frac{1}{\alpha^{n+1}}
\end{split}
\\]

其中$n\in\boldsymbol{N}$，由此得到：

\begin{equation}
\label{eq:50}
H\_+=\frac{e^2}{8\pi\varepsilon\_0}\frac{\widehat{N}^2}{V}\frac{4\pi}{\alpha^2}
\end{equation}

可见，当$\alpha\to0$时$H\_+$确实发散，但它会和其他项抵消掉。\eqref{eq:47}中的$H\_\text{e+}$表示电子和均匀离子背景之间的作用：

\begin{equation}
\label{eq:51}
H\_\text{e+}=-\frac{e^2}{4\pi\varepsilon\_0}\sum\_{i=1}^{N}\int\mathrm{d}^3r\frac{n(\boldsymbol{r})}{|\boldsymbol{r}-\boldsymbol{r}\_i|}e^{-\alpha|\boldsymbol{r}-\boldsymbol{r}\_i|}
\end{equation}

和计算$H\_+$一样，得到：

\\[
\begin{split}
H\_\text{e+}=&-\frac{e^2}{4\pi\varepsilon\_0}\frac{N}{V}\sum\_{i=1}^{N}\int\mathrm{d}^3r\frac{e^{-\alpha|\boldsymbol{r}-\boldsymbol{r}\_i|}}{|\boldsymbol{r}-\boldsymbol{r}\_i|}=\\\
=&-\frac{e^2}{4\pi\varepsilon\_0}\frac{N}{V}\sum\_{i=1}^{N}\frac{4\pi}{\alpha^2}
\end{split}
\\]

把粒子数$N$替换为粒子数算符$\widehat{N}$得到：

\begin{equation}
\label{eq:52}
H\_\text{e+}=-\frac{e^2}{4\pi\varepsilon\_0}\frac{\widehat{N}^2}{V}\frac{4\pi}{\alpha^2}
\end{equation}

合起来就是：

\begin{equation}
\label{eq:53}
H=H\_\text{e}-\frac{1}{2}\frac{e^2}{4\pi\varepsilon\_0}\frac{\widehat{N}^2}{V}\frac{4\pi}{\alpha^2}
\end{equation}

当$\alpha\to0$时依然发散，但我们将看到，$H\_\text{e}$中正好有一项能和上式第二项抵消。事实上，$H\_\text{e}$是最关键的算符，根据\eqref{eq:2}，其包含动能项$H\_0$\eqref{eq:7}和库伦作用项$H\_\text{ee}$\eqref{eq:43}。$H\_0$已经在前面完成二次量子化了。$H\_\text{ee}$是个典型的两体算符，根据[式(214)-二次量子化](/blog/second-quantisation#mjx-eqn-eq214)，其在Bloch表象中为：

\begin{equation}
\label{eq:54}
H\_\text{ee}=\frac{1}{2}\sum\_{\substack{\boldsymbol{k}\_1\cdots\boldsymbol{k}\_4\\\ \sigma\_1\cdots\sigma\_4}}v(\boldsymbol{k}\_1\sigma\_1,\ldots,\boldsymbol{k}\_4\sigma\_4)a\_{\boldsymbol{k}\_1\sigma\_1}^\dagger a\_{\boldsymbol{k}\_2\sigma\_2}^\dagger a\_{\boldsymbol{k}\_4\sigma\_4}a\_{\boldsymbol{k}\_3\sigma\_3}
\end{equation}

矩阵元

\\[
\begin{split}
&v(\boldsymbol{k}\_1\sigma\_1,\ldots,\boldsymbol{k}\_4\sigma\_4)=\\\
=&\frac{e^2}{4\pi\varepsilon\_0}\left\langle(\boldsymbol{k}\_1\sigma\_1)^{(1)}(\boldsymbol{k}\_2\sigma\_2)^{(2)}\left|\frac{1}{|\hat{\boldsymbol{r}}^{(1)}-\hat{\boldsymbol{r}}^{(2)}|}\right|(\boldsymbol{k}\_3\sigma\_3)^{(1)}(\boldsymbol{k}\_4\sigma\_4)^{(2)}\right\rangle
\end{split}
\\]

只有在$\sigma\_1=\sigma\_3$和$\sigma\_2=\sigma\_4$才不为零，由于算符本身与自旋无关：

\\[
\begin{split}
v(\boldsymbol{k}\_1\sigma\_1,\ldots,\boldsymbol{k}\_4\sigma\_4)&=\frac{e^2}{4\pi\varepsilon\_0}\iint\mathrm{d}^3r\_1\,\mathrm{d}^3r\_2\Big\langle\boldsymbol{k}\_1^{(1)}\boldsymbol{k}\_2^{(2)}\Big|\frac{1}{|\hat{\boldsymbol{r}}^{(1)}-\hat{\boldsymbol{r}}^{(2)}|}\cdot\\\
&\cdot\Big|\boldsymbol{r}\_1^{(1)}\boldsymbol{r}\_2^{(2)}\Big\rangle\Big\langle\boldsymbol{r}\_1^{(1)}\boldsymbol{r}\_2^{(2)}\Big|\boldsymbol{k}\_3^{(1)}\boldsymbol{k}\_4^{(2)}\Big\rangle\delta\_{\sigma\_1\sigma\_2}\delta\_{\sigma\_3\sigma\_4}=\\\
&=\frac{e^2}{4\pi\varepsilon\_0}\iint\mathrm{d}^3r\_1\,\mathrm{d}^3r\_2\frac{1}{|\boldsymbol{r}\_1-\boldsymbol{r}\_2|}\Big\langle\boldsymbol{k}\_1^{(1)}\boldsymbol{k}\_2^{(2)}\Big|\boldsymbol{r}\_1^{(1)}\boldsymbol{r}\_2^{(2)}\Big\rangle\cdot\\\
&\cdot\Big\langle\boldsymbol{r}\_1^{(1)}\boldsymbol{r}\_2^{(2)}\Big|\boldsymbol{k}\_3^{(1)}\boldsymbol{k}\_4^{(2)}\Big\rangle\delta\_{\sigma\_1\sigma\_2}\delta\_{\sigma\_3\sigma\_4}=\\\
&=\frac{e^2}{4\pi\varepsilon\_0}\iint\mathrm{d}^3r\_1\,\mathrm{d}^3r\_2\frac{1}{|\boldsymbol{r}\_1-\boldsymbol{r}\_2|}\psi\_{\boldsymbol{k}\_1}^\*(\boldsymbol{r}\_1)\psi\_{\boldsymbol{k}\_2}^\*(\boldsymbol{r}\_2)\cdot\\\
&\cdot\psi\_{\boldsymbol{k}\_3}(\boldsymbol{r}\_1)\psi\_{\boldsymbol{k}\_4}(\boldsymbol{r}\_2)\delta\_{\sigma\_1\sigma\_2}\delta\_{\sigma\_3\sigma\_4}
\end{split}
\\]

利用Bloch定理\eqref{eq:15}，可进一步发现：

\\[
\boldsymbol{k}\_1+\boldsymbol{k}\_2=\boldsymbol{k}\_3+\boldsymbol{k}\_4
\\]

这只需通过简单的变量替换便能看到。于是得到：

\begin{align}
\label{eq:55}
\begin{split}
v(\boldsymbol{k}\_1\sigma\_1,\ldots,\boldsymbol{k}\_4\sigma\_4)=&\delta\_{\sigma\_1\sigma\_2}\delta\_{\sigma\_3\sigma\_4}\delta\_{\boldsymbol{k}\_1+\boldsymbol{k}\_2,\boldsymbol{k}\_3+\boldsymbol{k}\_4}v(\boldsymbol{k}\_1,\ldots,\boldsymbol{k}\_4),\\\
v(\boldsymbol{k}\_1,\ldots,\boldsymbol{k}\_4)=&\frac{e^2}{4\pi\varepsilon\_0}\iint\mathrm{d}^3r\_1\,\mathrm{d}^3r\_2\psi\_{\boldsymbol{k}\_1}^\*(\boldsymbol{r}\_1)\psi\_{\boldsymbol{k}\_2}^\*(\boldsymbol{r}\_2)\cdot\\\
&\cdot\frac{1}{|\boldsymbol{r}\_1-\boldsymbol{r}\_2|}\psi\_{\boldsymbol{k}\_3}(\boldsymbol{r}\_1)\psi\_{\boldsymbol{k}\_4}(\boldsymbol{r}\_2)
\end{split}
\end{align}

对库伦作用项$H\_\text{ee}$，便得到如下表达式：

\begin{equation}
\label{eq:56}
H\_\text{ee}=\frac{1}{2}\sum\_{\substack{\boldsymbol{k}\_1,\ldots,\boldsymbol{k}\_4\\\ \sigma,\sigma'}}v(\boldsymbol{k}\_1,\ldots,\boldsymbol{k}\_4)\delta\_{\boldsymbol{k}\_1+\boldsymbol{k}\_2,\boldsymbol{k}\_3+\boldsymbol{k}\_4}a\_{\boldsymbol{k}\_1\sigma}^\dagger a\_{\boldsymbol{k}\_2\sigma'}^\dagger a\_{\boldsymbol{k}\_4\sigma'}a\_{\boldsymbol{k}\_3\sigma}
\end{equation}

在凝胶模型中，$\psi\_{\boldsymbol{k}}(\boldsymbol{r})$是平面波，所以作如下计算：

\begin{align}
\label{eq:57}
\begin{split}
&v\_\alpha(\boldsymbol{k}\_1,\ldots,\boldsymbol{k}\_4)=\\\
=&\frac{e^2}{4\pi\varepsilon\_0}\frac{1}{V^2}\iint\mathrm{d}^3r\_1\,\mathrm{d}^3r\_2\frac{e^{-i(\boldsymbol{k}\_1-\boldsymbol{k}\_3)\cdot\boldsymbol{r}\_1}e^{-i(\boldsymbol{k}\_2-\boldsymbol{k}\_4)\cdot\boldsymbol{r}\_2}}{|\boldsymbol{r}\_1-\boldsymbol{r}\_2|}e^{-\alpha|\boldsymbol{r}\_1-\boldsymbol{r}\_2|}
\end{split}
\end{align}

令

\begin{align}
\label{eq:58}
\begin{split}
&\boldsymbol{r}=\boldsymbol{r}\_1-\boldsymbol{r}\_2;\qquad&\boldsymbol{R}=\frac{1}{2}(\boldsymbol{r}\_1+\boldsymbol{r}\_2)\\\
\Longleftrightarrow&\boldsymbol{r}\_1=\frac{1}{2}\boldsymbol{r}+\boldsymbol{R};\qquad&\boldsymbol{r}\_2=-\frac{1}{2}\boldsymbol{r}+\boldsymbol{R}
\end{split}
\end{align}

雅可比行列式为$1$，接着计算：

\\[
\begin{split}
v\_\alpha(\boldsymbol{k}\_1,\ldots,\boldsymbol{k}\_4)=&\frac{e^2}{4\pi\varepsilon\_0}\frac{1}{V}\int\mathrm{d}^3R\,e^{-i(\boldsymbol{k}\_1-\boldsymbol{k}\_3+\boldsymbol{k}\_2-\boldsymbol{k}\_4)\cdot\boldsymbol{R}}\cdot\\\
&\cdot\frac{1}{V}\int\mathrm{d}^3r\,\frac{1}{r}e^{-\alpha r}e^{-(i/2)(\boldsymbol{k}\_1-\boldsymbol{k}\_3-\boldsymbol{k}\_2+\boldsymbol{k}\_4)\cdot\boldsymbol{r}}=\\\
=&\frac{e^2}{4\pi\varepsilon\_0}\delta\_{\boldsymbol{k}\_1+\boldsymbol{k}\_2,\boldsymbol{k}\_3+\boldsymbol{k}\_4}\frac{1}{V}\int\mathrm{d}^3r\,\frac{e^{-i(\boldsymbol{k}\_1-\boldsymbol{k}\_3)\cdot\boldsymbol{r}}e^{-\alpha r}}{r}
\end{split}
\\]

利用

\begin{align}
\label{eq:59}
\begin{split}
\int\mathrm{d}^3r\,\frac{e^{-i\boldsymbol{q}\cdot\boldsymbol{r}}}{r}e^{-\alpha r}&=\int\_0^{2\pi}\mathrm{d}\phi\int\_0^\infty\mathrm{d}r\int\_0^\pi\mathrm{d}\theta\,r^2\sin\theta\frac{e^{iqr\cos\theta}}{r}e^{-\alpha r}=\\\
&=2\pi\int\_0^\infty\mathrm{d}r\int\_0^\pi\mathrm{d}(\cos\theta)\left(-re^{iqr\cos\theta}e^{-\alpha r}\right)=\\\
&=2\pi\int\_0^\infty\mathrm{d}r\left[\frac{e^{iqr\cos\theta}}{-iq}\right]\_0^\pi e^{-\alpha r}=\\\
&=2\pi\int\_0^\infty\mathrm{d}r\frac{-1}{iq}\left(e^{-(\alpha+iq)r}-e^{-(\alpha-iq)r}\right)=\\\
&=2\pi\frac{-1}{iq}\left(\frac{1}{\alpha+iq}-\frac{1}{\alpha-iq}\right)=\\\
&=\frac{4\pi}{q^2+\alpha^2}
\end{split}
\end{align}

上式在极坐标中将$\boldsymbol{q}$固定于$z$轴。最终得到：

\begin{equation}
\label{eq:60}
v\_\alpha(\boldsymbol{k}\_1,\ldots,\boldsymbol{k}\_4)=\frac{e^2}{\varepsilon\_0V[(\boldsymbol{k}\_1-\boldsymbol{k}\_3)^2+\alpha^2]}\delta\_{\boldsymbol{k}\_1-\boldsymbol{k}\_3,\boldsymbol{k}\_4-\boldsymbol{k}\_2}
\end{equation}

代入\eqref{eq:56}得到：

\begin{gather}
\label{eq:61}
H\_\text{ee}^{(\alpha)}=\frac{1}{2}\sum\_{\substack{\boldsymbol{k},\boldsymbol{p},\boldsymbol{q}\\\ \sigma,\sigma'}}v\_\alpha(\boldsymbol{q})a\_{\boldsymbol{k}+\boldsymbol{q}\sigma}^\dagger a\_{\boldsymbol{p}-\boldsymbol{q}\sigma'}^\dagger a\_{\boldsymbol{p}\sigma'}a\_{\boldsymbol{k}\sigma},\\\
\label{eq:62}
v\_\alpha(\boldsymbol{q})=\frac{e^2}{\varepsilon\_0V(q^2+\alpha^2)}
\end{gather}

考虑库伦作用中$q=0$的项：

\begin{align}
\begin{split}
&\frac{1}{2}\frac{e^2}{\varepsilon\_0V\alpha^2}\sum\_{\substack{\boldsymbol{k},\boldsymbol{p}\\\ \sigma,\sigma'}}a\_{\boldsymbol{k}\sigma}^\dagger a\_{\boldsymbol{p}\sigma'}^\dagger a\_{\boldsymbol{p}\sigma'}a\_{\boldsymbol{k}\sigma}=\\\
&=\frac{1}{2}\frac{e^2}{\varepsilon\_0V\alpha^2}\sum\_{\substack{\boldsymbol{k},\boldsymbol{p}\\\ \sigma,\sigma'}}a\_{\boldsymbol{p}\sigma'}^\dagger\left(-a\_{\boldsymbol{k}\sigma}^\dagger a\_{\boldsymbol{p}\sigma'}\right)a\_{\boldsymbol{k}\sigma}=\\\
&=\frac{1}{2}\frac{e^2}{\varepsilon\_0V\alpha^2}\sum\_{\substack{\boldsymbol{k},\boldsymbol{p}\\\ \sigma,\sigma'}}a\_{\boldsymbol{p}\sigma'}^\dagger\left(-\delta\_{\sigma\sigma'}\delta\_{\boldsymbol{k}\boldsymbol{p}}+a\_{\boldsymbol{p}\sigma'}a\_{\boldsymbol{k}\sigma}^\dagger\right)a\_{\boldsymbol{k}\sigma}=\\\
&=\frac{1}{2}\frac{e^2}{\varepsilon\_0V\alpha^2}\sum\_{\substack{\boldsymbol{k},\boldsymbol{p}\\\ \sigma,\sigma'}}\left(-\delta\_{\sigma\sigma'}\delta\_{\boldsymbol{k}\boldsymbol{p}}n\_{\boldsymbol{k}\sigma}+n\_{\boldsymbol{p}\sigma'}n\_{\boldsymbol{k}\sigma}\right)=\\\
&=\frac{e^2}{2\varepsilon\_0V\alpha^2}\left[-\widehat{N}+(\widehat{N})^2\right]
\end{split}
\label{eq:63}
\end{align}

上式利用了Bloch算符的基本对易关系。可见\eqref{eq:63}的第2项与\eqref{eq:53}相抵消，即$H\_+$的贡献被$H\_\text{e+}$消除了。当将能量平均到每个粒子时\eqref{eq:63}的第1项在热力学极限下也消失了：

\\[
-\frac{e^2}{2\varepsilon\_0V\alpha^2}\xrightarrow[N\to\infty;V\to\infty]{}0
\\]

所以一开始就可以丢掉。最后取极限$\alpha\to0$，得到

> **凝胶模型哈密顿量**：
>
> \begin{equation}
\label{eq:64}
H=\sum\_{\boldsymbol{k}\sigma}\varepsilon\_0(\boldsymbol{k})a\_{\boldsymbol{k}\sigma}^\dagger a\_{\boldsymbol{k}\sigma}+\frac{1}{2}\sum\_{\substack{\boldsymbol{k},\boldsymbol{p},\boldsymbol{q}\\\ \sigma,\sigma'}}^{q\neq0}v\_0(\boldsymbol{q})a\_{\boldsymbol{k}+\boldsymbol{q}\sigma}^\dagger a\_{\boldsymbol{p}-\boldsymbol{q}\sigma'}^\dagger a\_{\boldsymbol{p}\sigma'}a\_{\boldsymbol{k}\sigma}
\end{equation}

从\eqref{eq:26}可见

\begin{equation}
\label{eq:65}
\varepsilon\_0(\boldsymbol{k})=\frac{\hbar^2k^2}{2m}
\end{equation}

为动能的矩阵元，而

\begin{equation}
\label{eq:66}
v\_0(\boldsymbol{q})=\frac{1}{V}\frac{e^2}{\varepsilon\_0q^2}
\end{equation}

属于库伦作用。

除此之外，再导出一种$H$的常用表示，用到了

> **电子密度算符**：
>
> \begin{equation}
\label{eq:67}
\hat{\rho}(\boldsymbol{r})=\sum\_{i=1}^{N}\delta(\boldsymbol{r}-\hat{\boldsymbol{r}}\_i)
\end{equation}

这是个单粒子算符。电子位置$\hat{\boldsymbol{r}}\_i$是算符，而变量$\boldsymbol{r}$自然不是。根据[式(214)-二次量子化](/blog/second-quantisation#mjx-eqn-eq214)，其在Bloch表象中为：

\begin{equation}
\label{eq:68}
\hat{\rho}(\boldsymbol{r})=\sum\_{\substack{\boldsymbol{k},\boldsymbol{k'}\\\ \sigma,\sigma'}}\langle\boldsymbol{k}\sigma|\delta(\boldsymbol{r}-\hat{\boldsymbol{r}})|\boldsymbol{k'}\sigma'\rangle a\_{\boldsymbol{k}\sigma}^\dagger a\_{\boldsymbol{k'}\sigma'}
\end{equation}

矩阵元作如下计算：

\\[
\begin{split}
\langle\boldsymbol{k}\sigma|\delta(\boldsymbol{r}-\hat{\boldsymbol{r}})|\boldsymbol{k'}\sigma'\rangle&=\sum\_{\sigma^{\prime\prime}}\int\mathrm{d}^3r^{\prime\prime}\langle\boldsymbol{k}\sigma|\delta(\boldsymbol{r}-\hat{\boldsymbol{r}})|\boldsymbol{r^{\prime\prime}}\sigma^{\prime\prime}\rangle\langle\boldsymbol{r^{\prime\prime}}\sigma^{\prime\prime}|\boldsymbol{k'}\sigma'\rangle=\\\
&=\sum\_{\sigma^{\prime\prime}}\int\mathrm{d}^3r^{\prime\prime}\delta(\boldsymbol{r}-\boldsymbol{r^{\prime\prime}})\langle\boldsymbol{k}\sigma|\boldsymbol{r^{\prime\prime}}\sigma^{\prime\prime}\rangle\langle\boldsymbol{r^{\prime\prime}}\sigma^{\prime\prime}|\boldsymbol{k'}\sigma'\rangle=\\\
&=\sum\_{\sigma^{\prime\prime}}\delta\_{\sigma\sigma^{\prime\prime}}\delta\_{\sigma^{\prime\prime}\sigma'}\langle\boldsymbol{k}\sigma|\boldsymbol{r}\sigma\rangle\langle\boldsymbol{r}\sigma|\boldsymbol{k'}\sigma\rangle=\\\
&=\delta\_{\sigma\sigma'}\psi\_\boldsymbol{k}^\*(\boldsymbol{r})\psi\_\boldsymbol{k'}(\boldsymbol{r})
\end{split}
\\]

如果像凝胶模型中一样，将Bloch函数限定为平面波，便得到

\begin{equation}
\label{eq:69}
\langle\boldsymbol{k}\sigma|\delta(\boldsymbol{r}-\hat{\boldsymbol{r}})|\boldsymbol{k'}\sigma'\rangle=\delta\_{\sigma\sigma'}\frac{1}{V}e^{i(\boldsymbol{k'}-\boldsymbol{k})\cdot\boldsymbol{r}}
\end{equation}

按照\eqref{eq:68}，这意味着：

\begin{equation}
\label{eq:70}
\hat{\rho}(\boldsymbol{r})=\frac{1}{V}\sum\_{\boldsymbol{k},\boldsymbol{q},\sigma}a\_{\boldsymbol{k}\sigma}^\dagger a\_{\boldsymbol{k+q}\sigma}e^{i\boldsymbol{q}\cdot\boldsymbol{r}}
\end{equation}

作傅里叶变换得到：

\begin{equation}
\label{eq:71}
\hat{\rho}\_\boldsymbol{q}=\sum\_{\boldsymbol{k},\sigma}a\_{\boldsymbol{k}\sigma}^\dagger a\_{\boldsymbol{k+q}\sigma}
\end{equation}

可以看出：

\begin{equation}
\label{eq:72}
\hat{\rho}\_\boldsymbol{q}^\dagger=\hat{\rho}\_\boldsymbol{-q};\qquad\hat{\rho}\_\boldsymbol{q=0}=\widehat{N}
\end{equation}

稍加计算也能发现：

\\[
\begin{split}
\hat{\rho}\_\boldsymbol{q}\hat{\rho}\_\boldsymbol{-q}&=\sum\_{\boldsymbol{k}\sigma}a\_{\boldsymbol{k}\sigma}^\dagger a\_{\boldsymbol{k+q}\sigma}\sum\_{\boldsymbol{p}\sigma'}a\_{\boldsymbol{p}\sigma'}^\dagger a\_{\boldsymbol{p-q}\sigma'}=\\\
&=\sum\_{\substack{\boldsymbol{k},\boldsymbol{p}\\\ \sigma,\sigma'}}a\_{\boldsymbol{k}\sigma}^\dagger a\_{\boldsymbol{k+q}\sigma}a\_{\boldsymbol{p}\sigma'}^\dagger a\_{\boldsymbol{p-q}\sigma'}=\\\
&=\sum\_{\substack{\boldsymbol{k},\boldsymbol{p}\\\ \sigma,\sigma'}}a\_{\boldsymbol{k}\sigma}^\dagger\left(\delta\_{\boldsymbol{k+q},\boldsymbol{p}}\delta\_{\sigma\sigma'}-a\_{\boldsymbol{p}\sigma'}^\dagger a\_{\boldsymbol{k+q}\sigma}\right)a\_{\boldsymbol{p-q}\sigma'}=\\\
&=\sum\_{\boldsymbol{k}\sigma}a\_{\boldsymbol{k}\sigma}^\dagger a\_{\boldsymbol{k}\sigma}-\sum\_{\substack{\boldsymbol{k},\boldsymbol{p}\\\ \sigma,\sigma'}}a\_{\boldsymbol{p}\sigma'}^\dagger a\_{\boldsymbol{k}\sigma}^\dagger a\_{\boldsymbol{p-q}\sigma'}a\_{\boldsymbol{k+q}\sigma}=\\\
&=\widehat{N}-\sum\_{\substack{\boldsymbol{k},\boldsymbol{p}\\\ \sigma,\sigma'}}a\_{\boldsymbol{p}\sigma'}^\dagger\left(\delta\_{\boldsymbol{k},\boldsymbol{p-q}}\delta\_{\sigma\sigma'}-a\_{\boldsymbol{p-q}\sigma'}a\_{\boldsymbol{k}\sigma}^\dagger\right)a\_{\boldsymbol{k+q}\sigma}=\\\
&=\widehat{N}-\sum\_{\boldsymbol{p}\sigma}a\_{\boldsymbol{p}\sigma}^\dagger a\_{\boldsymbol{p}\sigma}+\sum\_{\boldsymbol{p}\sigma'}a\_{\boldsymbol{p}\sigma'}^\dagger a\_{\boldsymbol{p-q}\sigma'}\sum\_{\boldsymbol{k}\sigma}a\_{\boldsymbol{k}\sigma}^\dagger a\_{\boldsymbol{k+q}\sigma}=\\\
&=\hat{\rho}\_\boldsymbol{-q}\hat{\rho}\_\boldsymbol{q}
\end{split}
\\]

即

\\[
[\hat{\rho}\_\boldsymbol{q},\hat{\rho}\_\boldsymbol{-q}]=0
\\]

据此可将凝胶模型的哈密顿量用密度算符表示，动能项不变：

\\[
\begin{split}
H\_\text{ee}=&\frac{1}{2}\sum\_{\substack{\boldsymbol{k},\boldsymbol{p},\boldsymbol{q}\\\ \sigma,\sigma'}}^{q\neq0}v\_0(\boldsymbol{q})a\_{\boldsymbol{k}+\boldsymbol{q}\sigma}^\dagger a\_{\boldsymbol{p}-\boldsymbol{q}\sigma'}^\dagger a\_{\boldsymbol{p}\sigma'}a\_{\boldsymbol{k}\sigma}=\\\
=&\frac{1}{2}\sum\_{\substack{\boldsymbol{k},\boldsymbol{p},\boldsymbol{q}\\\ \sigma,\sigma'}}^{q\neq0}v\_0(\boldsymbol{q})a\_{\boldsymbol{k}+\boldsymbol{q}\sigma}^\dagger\left(-\delta\_{\sigma\sigma'}\delta\_{\boldsymbol{k},\boldsymbol{p-q}}+a\_{\boldsymbol{k}\sigma}a\_{\boldsymbol{p-q}\sigma'}^\dagger\right)a\_{\boldsymbol{p}\sigma'}=\\\
=&-\frac{1}{2}\sum\_{\boldsymbol{q},\boldsymbol{p},\sigma}^{q\neq0}v\_0(\boldsymbol{q})a\_{\boldsymbol{p}\sigma}^\dagger a\_{\boldsymbol{p}\sigma}+\frac{1}{2}\sum\_{\boldsymbol{q}}^{q\neq0}v\_0(\boldsymbol{q})\sum\_{\boldsymbol{k},\sigma}a\_{\boldsymbol{k}+\boldsymbol{q}\sigma}^\dagger a\_{\boldsymbol{k}\sigma}\cdot\\\
&\cdot\sum\_{\boldsymbol{p},\sigma'}a\_{\boldsymbol{p-q}\sigma'}^\dagger a\_{\boldsymbol{p}\sigma'}
\end{split}
\\]

于是凝胶模型哈密顿量变成：

\begin{equation}
\label{eq:73}
H=\frac{1}{2}\sum\_{\boldsymbol{k}\sigma}\varepsilon\_0(\boldsymbol{k})a\_{\boldsymbol{k}\sigma}^\dagger a\_{\boldsymbol{k}\sigma}+\frac{1}{2}\sum\_{\boldsymbol{q}}^{q\neq0}v\_0(\boldsymbol{q})\left\\{\hat{\rho}\_\boldsymbol{q}^\dagger\hat{\rho}\_\boldsymbol{q}-\widehat{N}\right\\}
\end{equation}

为了深入了解此模型的*物理本质*，现在计算它的基态能。我们采用一阶微扰论，根据变分原理它能给出基态能的上界。将库伦相互作用$H\_\text{ee}$作为*微扰*；*未扰*系统便是（Sommerfeld模型）：

\begin{equation}
\label{eq:74}
H\_0=\frac{1}{2}\sum\_{\boldsymbol{k}\sigma}\varepsilon\_0(\boldsymbol{k})a\_{\boldsymbol{k}\sigma}^\dagger a\_{\boldsymbol{k}\sigma}
\end{equation}

有精确解。在

<p style="text-align: center"><b>"未扰"基态$|E\_0\rangle$</b></p>

中$N$个电子占据了小于限制能$\varepsilon\_F$的所有态，叫做**费米能**(Fermi energy)：

\begin{equation}
\label{eq:75}
\varepsilon\_0(\boldsymbol{k})a=\frac{\hbar^2k^2}{2m}\leq\varepsilon\_F=\frac{\hbar^2k\_F^2}{2m}
\end{equation}

$k\_F$叫做**费米波矢**(Fermi wavevector)，可由如下计算得到：由于能量色散各向同性

\begin{equation}
\label{eq:76}
\varepsilon\_0(\boldsymbol{k})=\varepsilon\_0(k)
\end{equation}

电子在$\boldsymbol{k}$空间占据半径为$k\_F$的球体中所有态。由于周期性边界条件\eqref{eq:46}$\boldsymbol{k}$空间中的$\boldsymbol{k}$-点是离散的，每个$\boldsymbol{k}$-点可占据

\begin{equation}
\label{eq:77}
\text{网格体积}\qquad\Delta k=\frac{(2\pi)^3}{L^3}=\frac{(2\pi)^3}{V}
\end{equation}

若是考虑自旋简并，便会得到电子数与费米波矢$k\_F$之间的关系：

$$
N=2\frac{1}{\Delta k}\left(\frac{4\pi}{3}k\_F^3\right)=\frac{V}{3\pi^2}k\_F^3
$$

即

\begin{gather}
\label{eq:78}
k\_F=\left(3\pi^2\frac{N}{V}\right)^{1/3}\\\
\label{eq:79}
\varepsilon\_F=\frac{\hbar^2}{2m}\left(3\pi^2\frac{N}{V}\right)^{2/3}
\end{gather}

每个粒子的平均能量$\bar{\varepsilon}$是：

\begin{equation}
\label{eq:80}
\bar{\varepsilon}=\frac{2}{N}\left(\int\_{k\leq k\_F}\mathrm{d}^3k\,\frac{\hbar^2k^2}{2m}\right)\frac{1}{\Delta k}=\frac{3}{5}\varepsilon\_F
\end{equation}

在热力学极限下上式用到了

\\[
\sum\_{\boldsymbol{k}}\to\frac{1}{\Delta \boldsymbol{k}}\int\mathrm{d}^3k
\\]

并考虑了自旋简并。于是得到基态能：

\begin{equation}
\label{eq:81}
E\_0=N\bar{\varepsilon}=\frac{3}{5}N\varepsilon\_F
\end{equation}

现介绍几个标准缩写(standard abbreviations)：

\begin{align}
\label{eq:83}
n\_\text{e}&=\frac{N}{V}:\quad&\text{平均电子密度}\\\
v\_\text{e}&=\frac{1}{n\_\text{e}}:\quad&\text{平均电子体积}\\\
\end{align}

$v\_\text{e}$由无量纲的**密度参数**(density parameter)$r\_s$决定：

\begin{equation}
\label{eq:84}
v\_\text{e}=\frac{4\pi}{3}(a\_Br\_s)^3
\end{equation}

其中

\begin{equation}
\label{eq:85}
a\_B=\frac{4\pi\varepsilon\_0\hbar^2}{me^2}=0.529\overset{\lower.5em\circ}{\mathrm{A}}
\end{equation}

为**玻尔半径**(Bohr radius)。以类似的方式引入能量参数

\begin{equation}
\label{eq:86}
1\,\textrm{ryd}=\frac{1}{4\pi\varepsilon\_0}\frac{e^2}{2a\_B}=13.605\,\textrm{eV}
\end{equation}

那么费米能$\varepsilon\_F$可表示成：

\begin{equation}
\label{eq:87}
\varepsilon\_F=\frac{\alpha^2}{r\_s^2}[\mathrm{ryd}];\quad\alpha=\left(\frac{9\pi}{4}\right)^{1/3}
\end{equation}

未扰基态能便是：

\begin{equation}
\label{eq:88}
E\_0=N\frac{2.21}{r\_s^2}[\mathrm{ryd}]
\end{equation}

现在加入微扰$H\_\text{ee}$并计算一阶能量修正：

\begin{equation}
\label{eq:89}
\varepsilon^{(1)}=\frac{1}{2N}\sum\_{\substack{\boldsymbol{k},\boldsymbol{p},\boldsymbol{q}\\\ \sigma,\sigma'}}^{q\neq0}v\_0(\boldsymbol{q})\Big\langle E\_0\Big|a\_{\boldsymbol{k}+\boldsymbol{q}\sigma}^\dagger a\_{\boldsymbol{p}-\boldsymbol{q}\sigma'}^\dagger a\_{\boldsymbol{p}\sigma'}a\_{\boldsymbol{k}\sigma}\Big|E\_0\Big\rangle
\end{equation}

上式中的产生湮灭算符作用于$\|E\_0\rangle$后，还须产生$\|E\_0\rangle$，否则与左矢内积为零，即湮灭算符作用于费米球**内**的态，而后产生算符填充这些球内的空穴，故只有以下两项对微扰修正有贡献：

**1)直接项**(Direct Term)：

\begin{equation}
\label{eq:90}
\boldsymbol{k}=\boldsymbol{k}+\boldsymbol{q};\quad\boldsymbol{p}=\boldsymbol{p}-\boldsymbol{q}\iff q=0
\end{equation}

基于之前的讨论，这种项不会在求和中出现！

**2)交换项**(Exchange Term)：

\begin{equation}
\label{eq:91}
\sigma=\sigma';\quad\boldsymbol{k}+\boldsymbol{q}=\boldsymbol{p};\quad\boldsymbol{p}-\boldsymbol{q}=\boldsymbol{k}
\end{equation}

这是典型的量子力学的项，并没有经典对应。它来源于$N$-粒子态的反对称化原理：

\begin{align}
\label{eq:92}
\begin{split}
\varepsilon^{(1)}&=\frac{1}{2N}\sum\_{\boldsymbol{k},\boldsymbol{q},\sigma}^{q\neq0}v\_0(\boldsymbol{q})\Big\langle E\_0\Big|a\_{\boldsymbol{k}+\boldsymbol{q}\sigma}^\dagger a\_{\boldsymbol{p}-\boldsymbol{q}\sigma'}^\dagger a\_{\boldsymbol{p}\sigma'}a\_{\boldsymbol{k}\sigma}\Big|E\_0\Big\rangle=\\\
&=-\frac{1}{2N}\sum\_{\boldsymbol{k},\boldsymbol{q},\sigma}^{q\neq0}v\_0(\boldsymbol{q})\Big\langle E\_0\Big|\hat{n}\_{\boldsymbol{k}+\boldsymbol{q}\sigma} \hat{n}\_{\boldsymbol{k}\sigma}\Big|E\_0\Big\rangle
\end{split}
\end{align}

由于在*未扰*基态$\|E\_0\rangle$，费米球内的所有态都被占据而球外都没被占据，便有：

\begin{equation}
\label{eq:93}
\varepsilon^{(1)}=-\frac{1}{2N}\sum\_{\boldsymbol{k},\boldsymbol{q},\sigma}^{q\neq0}v\_0(\boldsymbol{q})\varTheta(k\_F-|\boldsymbol{k}+\boldsymbol{q}|)\varTheta(k\_F-k)
\end{equation}

在对自旋求和之后，将求和变积分：

\\[
\varepsilon^{(1)}=-\frac{V}{N}\frac{e^2}{\varepsilon\_0(2\pi)^6}\int\mathrm{d}^3k\int\mathrm{d}^3q\,\frac{1}{q^2}\varTheta(k\_F-|\boldsymbol{k}+\boldsymbol{q}|)\varTheta(k\_F-k)
\\]

做替换

\\[
\boldsymbol{k}\Rightarrow\boldsymbol{x}=\boldsymbol{k}+\frac{1}{2}\boldsymbol{q}
\\]

便得到

\begin{align}
\label{eq:94}
\varepsilon^{(1)}&=-\frac{V}{N}\frac{e^2}{\varepsilon\_0(2\pi)^6}\int\mathrm{d}^3q\,\frac{1}{q^2}2S(q)\\\
\label{eq:95}
S(q)&=\frac{1}{2}\int\mathrm{d}^3x\,\varTheta\left(k\_F-\left|\boldsymbol{x}+\frac{1}{2}\boldsymbol{q}\right|\right)\varTheta\left(k\_F-\left|\boldsymbol{x}-\frac{1}{2}\boldsymbol{q}\right|\right)
\end{align}

由[图 3](#fig-3)中的球缺(spherical segment)示意图易得：

\begin{equation}
\label{eq:96}
S(q)=\varTheta\left(k\_F-\frac{1}{2}q\right)\left\\{k\_F^3-\frac{3}{4}qk\_F^2+\frac{1}{16}q^3\right\\}
\end{equation}

此处用到球缺的体积公式：

\\[
S= \pi \times h^2\times(R-\frac{h}{3})= \pi \times h \times\frac{3r^2+h^2}{6} 
\\]

这里$R$是球体的半径，$h$是球缺的高，$r$是底面半径。再代入\eqref{eq:94}中即可得到：

\\[
\varepsilon^{(1)}=-\frac{0.916}{r\_s}[\mathrm{ryd}]
\\]

<figure id="fig-3">
  <img src="{{ '2018-03-27-many-body-model-systems-spherical-segment.png' | prepend:'/upload/posts/' | relative_url }}" alt="spherical segment">
  <figcaption><b>图 3</b>球缺积分区域示意图。</figcaption>
</figure>

最终得到单粒子的基态能：

\begin{equation}
\label{eq:97}
\frac{1}{N}E\_\text{min}[\mathrm{ryd}]=\frac{2.21}{r\_s^2}-\frac{0.916}{r\_s}+\varepsilon\_\text{corr}=\varepsilon
\end{equation}

第一项是动能\eqref{eq:88}，第二项即所谓**交换能**(exchange energy)。后者为全同粒子系统的典型特征，也是不可分辨性原理的直接结果，对于费米子来说就是泡利不相容原理。它保证自旋相同的电子不会靠得太近。所有使相同电荷的粒子保持*一定距离*的效应都会降低其基态能。这也是\eqref{eq:97}中负号的来源，相当于一种引力，当$r\_s$取适当值时，系统处于束缚态。最后一项叫做**关联能**(correlation energy)。它给出微扰论所得能量与精确结果之间的误差，因此自然是未知的。现代多体理论方法给出如下展开式：

\begin{equation}
\label{eq:98}
\varepsilon\_\text{corr}=\frac{2}{\pi^2}(1-\ln2)\ln r\_s-0.094+O(r\_s\ln r\_s)[\mathrm{ryd}]
\end{equation}

这样一个简单的凝胶模型已经给出了有用的结果，比如，$\varepsilon-\varepsilon\_\text{corr}$在

\\[
\begin{split}
r\_0=(r\_s)\_\text{min}&=4.83,\\\
(\varepsilon-\varepsilon\_\text{corr})\_\text{min}&=-0.095[\mathrm{ryd}]=-1.29[\mathrm{eV}]
\end{split}
\\]

这意味着电子密度的最优值，对应着最佳离子间距，并至少是定性地解释了**金属键**(metallic bonding)。

### 1.3 Hubbard模型
凝胶模型的简化关键在于其忽略了晶格结构，将离子视作均匀分布的正电荷背景。于是Bloch函数成了平面波\eqref{eq:45}，在整个晶体中电子的占有几率是个常数。胶体模型从一开始就只限于*宽*能带电子，比如碱金属的导带电子。

对于*窄*能带电子，其迁移率相对较低，其在晶格离子处的占有几率与宽能带电子大不一样。平面波自然不再适用于这种能带结构的电子。一个好得多的出发点是所谓**紧束缚近似**(tight-binding approximation)。紧束缚近似适用于这类情况：原子波函数之间的重叠足够大以至于需要对独立原子的构象进行修正，但还没有大到完全与原子波函数的描述无关。它最适用于过渡金属半填满的$d$-壳层以及描述绝缘体的电子结构。

假定晶格势$\widehat{V}(\boldsymbol{r})$很强且带电子的迁移率很低，在格点附近，原子哈密顿量

\begin{equation}
\label{eq:99}
H\_\text{at}=\sum\_{i=1}^{N\_\text{i}}h\_\text{at}^{(i)}
\end{equation}

是独立原子的哈密顿量之和，应当是整个周期性晶格哈密顿量的不错的近似，它和$H\_0$\eqref{eq:7}非常相似：

\begin{equation}
\label{eq:100}
h\_\text{at}^{(i)}\varphi\_n(\boldsymbol{r}-\boldsymbol{R}\_i)=\varepsilon\_n\varphi\_n(\boldsymbol{r}-\boldsymbol{R}\_i)
\end{equation}

这里$\varphi\_n$是原子波函数，视为已知。指数$n$象征一组量子数。其次假定$\varphi\_n$非常局域化，超过“一定范围”就变得非常小。集中于$\boldsymbol{R}\_i$，$\boldsymbol{R}\_j$处的波函数之间重叠非常小，这源于不同原子间电子的隧穿几率很小，原子能级劈裂很小，即窄能带。

在极端情况下，晶体哈密顿量只有在超过一定范围（此时原子波函数为零）才和$H\_\text{at}$产生差别，于是$\varphi\_n$便是整个哈密顿量定态波函数很好的近似。

对于无相互作用的电子哈密顿量\eqref{eq:7}，

\begin{equation}
\label{eq:101}
H\_0=\sum\_{i=1}^{N\_\text{e}}h\_0^{(i)}
\end{equation}

为了计算对于极端情况的修正，采用如下晶格哈密顿量：

\begin{equation}
\label{eq:102}
h\_0=h\_\text{at}+V\_1(\boldsymbol{r})
\end{equation}

这里$V\_1(\boldsymbol{r})$包含了由原子周期势产生真实晶体周期势所需的所有修正。
如果$\varphi\_n$满足薛定谔方程\eqref{eq:100}，它必然也满足

\begin{equation}
\label{eq:103}
h\_0\psi\_{n\boldsymbol{k}}(\boldsymbol{r})=\varepsilon\_n(\boldsymbol{k})\psi\_{n\boldsymbol{k}}(\boldsymbol{r})
\end{equation}

前提是，任何$\varphi\_n(\boldsymbol{r})$存在的地方$V\_1(\boldsymbol{r})$都消失。若果是这种情况，每个原子能级$\varphi\_n(\boldsymbol{r})$在周期势中都会贡献$N\_\text{i}$个能级，对$N\_\text{i}$个晶格$\boldsymbol{R}\_i$中的每一个都会有波函数$\varphi\_n(\boldsymbol{r}-\boldsymbol{R}\_i)$。在满足Bloch定理\eqref{eq:15}的条件下，这$N\_\text{i}$个简并波函数的线性组合成试探Bloch函数解

\begin{equation}
\label{eq:104}
\psi\_{n\boldsymbol{k}}(\boldsymbol{r})=\frac{1}{\sqrt{N\_\text{i}}}\sum\_{j=1}^{N\_\text{i}}e^{i\boldsymbol{k}\cdot\boldsymbol{R}\_j}\varphi\_n(\boldsymbol{r}-\boldsymbol{R}\_j)
\end{equation}

此函数保留了原子能级的特征。这种方法得到的能带没什么结构，$\varepsilon\_n(\boldsymbol{k})$仅仅是简单的原子能级$\varepsilon\_n$，与$\boldsymbol{k}$的取值无关。为了弥补这种不足，更实际的假设应当是：在$V\_1(\boldsymbol{r})$变得相当可观之前，$\varphi\_n(\boldsymbol{r})$变小，但没完全消失。这启示我们寻找一个满足整个晶体的薛定谔方程的解，其形式仍然符合\eqref{eq:104}：

\\[
\psi(\boldsymbol{r})=\frac{1}{\sqrt{N\_\text{i}}}\sum\_{j=1}^{N\_\text{i}}e^{i\boldsymbol{k}\cdot\boldsymbol{R}\_j}\phi(\boldsymbol{r}-\boldsymbol{R}\_j)
\\]

这里$\phi(\boldsymbol{r})$不一定正好是一个定态原子波函数，它需要由后续计算确定。如果乘积$V\_1(\boldsymbol{r})\varphi\_n(\boldsymbol{r})$虽然不为零，但也足够小，有理由期望$\phi(\boldsymbol{r})$与原子波函数$\varphi\_n(\boldsymbol{r})$或者与$\varphi\_n(\boldsymbol{r})$简并的波函数非常接近。基于此，$\phi(\boldsymbol{r})$可由少数几个局域原子波函数的线性展出：

\\[
\phi(\boldsymbol{r})=\sum\_n b\_n\varphi\_n(\boldsymbol{r})
\\]

> **附注**：  
> 1. 我们的第一次严格近似是只包含局域的（即束缚的）原子波函数。一组完整的原子能级应当包含电离了的原子。这也是该方法不能用于近自由电子能级的原因。
> 2. 因为这种对$\phi(\boldsymbol{r})$近似方式，紧束缚近似有时也被称作*原子轨道线性组合法*(linear combination of atomic orbits)（或LCAO）。

对比\eqref{eq:29}可见，我们把精确的Wannier函数替换成了束缚的原子波函数的组合。用$\varphi\_m^\*(\boldsymbol{r})$乘\eqref{eq:103}并对$\boldsymbol{r}$积分可得：

\\[
\int\mathrm{d}\boldsymbol{r}\,\varphi\_m^\*(\boldsymbol{r})h\_0\psi(\boldsymbol{r})=\int\mathrm{d}\boldsymbol{r}\,\varphi\_m^\*(\boldsymbol{r})\left(h\_\text{at}+V\_1(\boldsymbol{r})\right)\psi(\boldsymbol{r})=\varepsilon(\boldsymbol{k})\int\mathrm{d}\boldsymbol{r}\,\varphi\_m^\*(\boldsymbol{r})\psi(\boldsymbol{r})
\\]

再有：

\\[
\int\mathrm{d}\boldsymbol{r}\,\varphi\_m^\*(\boldsymbol{r})h\_\text{at}\psi(\boldsymbol{r})=\int\mathrm{d}\boldsymbol{r}\,\left(h\_\text{at}\varphi\_m(\boldsymbol{r})\right)^\*\psi(\boldsymbol{r})=\varepsilon\_m\int\mathrm{d}\boldsymbol{r}\,\varphi\_m^\*(\boldsymbol{r})\psi(\boldsymbol{r})
\\]

于是得到：

\\[
(\varepsilon(\boldsymbol{k})-\varepsilon\_m)\int\mathrm{d}\boldsymbol{r}\,\varphi\_m^\*(\boldsymbol{r})\psi(\boldsymbol{r})=\int\mathrm{d}\boldsymbol{r}\,\varphi\_m^\*(\boldsymbol{r})V\_1(\boldsymbol{r})\psi(\boldsymbol{r})
\\]

将$\psi(\boldsymbol{r})$展开式代入上式，并利用原子波函数的正交性：

\\[
\int\mathrm{d}\boldsymbol{r}\,\varphi\_m^\*(\boldsymbol{r})\varphi\_n(\boldsymbol{r})=\delta\_{mn}
\\]

最终得到如下本征方程，解此方程可得到系数$b\_n(\boldsymbol{k})$和Bloch能$\varepsilon(\boldsymbol{k})$：

\begin{equation}
\begin{split}
(\varepsilon(\boldsymbol{k})-\varepsilon\_m)b\_m=&-(\varepsilon(\boldsymbol{k})-\varepsilon\_m)\sum\_n\left(\sum\_{\boldsymbol{R}\neq0}\int\mathrm{d}\boldsymbol{r}\,\varphi\_m^\*(\boldsymbol{r})\varphi\_n(\boldsymbol{r-R})e^{i\boldsymbol{k}\cdot\boldsymbol{R}}\right)b\_n+\\\
&+\sum\_n\left(\int\mathrm{d}\boldsymbol{r}\,\varphi\_m^\*(\boldsymbol{r})V\_1(\boldsymbol{r})\varphi\_n(\boldsymbol{r})\right)b\_n+\\\
&+\sum\_n\left(\sum\_{\boldsymbol{R}\neq0}\int\mathrm{d}\boldsymbol{r}\,\varphi\_m^\*(\boldsymbol{r})V\_1(\boldsymbol{r})\varphi\_n(\boldsymbol{r-R})e^{i\boldsymbol{k}\cdot\boldsymbol{R}})\right)b\_n
\end{split}
\label{eq:105}
\end{equation}

上式右边第一项包含此种形式的积分：

\\[
\int\mathrm{d}\boldsymbol{r}\,\varphi\_m^\*(\boldsymbol{r})\varphi\_n(\boldsymbol{r-R})
\\]

我们对于原子能级非常定域化的假设意味着该项非常小。

> **附注**：  
> 积分中包含对两个不同格点波函数的乘积的积分叫做*重叠积分*(overlap integrals)。紧束缚近似利用了重叠积分很小这一特性。该积分在磁性理论中也发挥重要作用。

\eqref{eq:105}第三项也很小，因为它也包含了重叠积分。最后，我们认为\eqref{eq:105}第二项很小因为我们期望当周期势偏离原子势时离格点已经足够远，而这时原子波函数已变得很小。

> **附注**：  
> 相比其他假设这个假设有点站不住脚，因为离子势衰减速度无需和原子波函数一样快。但是，这对最终结果并无致命影响，因为问题中该项并不依赖于$\boldsymbol{k}$。在某种意义上，该项的作用是修正元胞内的原子势以包含元胞外的离子场的影响；通过合理定义“原子”哈密顿量和能级，这一项也能变得和其他两项一样小。

最终发现\eqref{eq:105}右边（也即$(\varepsilon(\boldsymbol{k})-\varepsilon\_m)$）总是很小。这意味着每当$b\_m$不小的时候，$\varepsilon(\boldsymbol{k})-\varepsilon\_m$一定很小（反之亦然）。故$\varepsilon(\boldsymbol{k})$必须接近某个原子能级，比如$\varepsilon\_0$，所有的$b\_m$除了那些相应的能级能量与其简并（或非常接近）的都必须很小：

\\[
\varepsilon(\boldsymbol{k})\approx\varepsilon\_0,\quad b\_m\approx0\text{ unless  }\varepsilon\_m\approx\varepsilon\_0
\\]

如果上式为严格的等式，我们又会回到极端情况，晶体能级与原子能级相同。利用上式，我们可以将\eqref{eq:105}右侧求和指标$n$限定于那些能级能量与$\varepsilon\_0$简并或者非常接近的几个，\eqref{eq:105}便成了一个分块对角矩阵方程。如果原子能级$0$是非简并的，即$s$能级（这里没有考虑SOC，只关注能级的轨道部分，自旋可通过在轨道波函数乘以相应自旋波函数引入，这样轨道能级简并度翻倍），在此近似下\eqref{eq:105}简化为由$s$能级（一般叫做“$s$带”）产生的能带能量的明确表达式。如果考虑$p$能级，它是三重简并的，\eqref{eq:105}便成为一组三个方程。同理，考虑$d$能级，就要解$5\times5$的矩阵方程。

如果解得的$\varepsilon(\boldsymbol{k})$在某些$\boldsymbol{k}$处离所考虑的原子能级足够远，那么就要重复以上步骤，将此时$\varepsilon(\boldsymbol{k})$所接近的能级也包括进$\phi$的展开式。实际上，在算过渡金属能带时常常要解包含了$s$-和$d$-能级的$6\times6$的方程，其原子态含有外层$s$-壳层及部分填充的$d$-壳层。此过程即所谓“$s$-$d$混合”或“杂化”。

通常原子波函数短程有效，\eqref{eq:105}中对$\boldsymbol{R}$的求和仅需保留近邻项，这对后续分析又大大简化。下面就举个最简单的$s$能级的例子。

如果\eqref{eq:105}中除了单个$s$能级的系数$b$剩下的全为零，便直接得到其相应$s$-带能带结构：

\begin{equation}
\label{eq:106}
\varepsilon\_n(\boldsymbol{k})=\varepsilon\_n+\frac{v\_n+\sum\_j^{\neq0}\gamma\_n^{(j)}e^{i\boldsymbol{k}\cdot\boldsymbol{R}\_j}}{1+\sum\_j^{\neq0}\alpha\_n^{(j)}e^{i\boldsymbol{k}\cdot\boldsymbol{R}\_j}}
\end{equation}

这里$\varepsilon\_n=\varepsilon\_s$为$s$-能级能量，并且

\begin{align}
\label{eq:107}
v\_n&=\int\mathrm{d}\boldsymbol{r}\,V\_1(\boldsymbol{r})|\varphi\_n(\boldsymbol{r})|^2\\\
\label{eq:108}
T\_0^{(n)}&=\varepsilon\_n+v\_n\\\
\label{eq:109}
\alpha\_n^{(j)}&=\int\mathrm{d}\boldsymbol{r}\,\varphi\_n^\*(\boldsymbol{r})\varphi\_n(\boldsymbol{r}-\boldsymbol{R}\_j)\\\
\label{eq:110}
\gamma\_n^{(j)}&=\int\mathrm{d}\boldsymbol{r}\,\varphi\_n^\*(\boldsymbol{r})V\_1(\boldsymbol{r})\varphi\_n(\boldsymbol{r}-\boldsymbol{R}\_j)
\end{align}

上面这些系数可据对称性进行简化。由于$\varphi\_n$为$s$-能级，它是实数且仅依赖于$r$的大小。由此可得$\alpha\_n(-\boldsymbol{R})=\alpha\_n(\boldsymbol{R})$。此外由于Bravais格子的空间反演对称性要求$V\_1(-\boldsymbol{R})=V\_1(\boldsymbol{R})$，便有$\gamma\_n(-\boldsymbol{R})=\gamma\_n(\boldsymbol{R})$。\eqref{eq:106}分母上的$\alpha$对分子的修正很小，故将其忽略。最后假设只有近邻重叠积分才有效，便得到最终简化形式：

\begin{equation}
\label{eq:111}
\varepsilon\_n(\boldsymbol{k})=T\_0^{(n)}+\sum\_\Delta \gamma\_n^{(1)}e^{i\boldsymbol{k}\cdot\boldsymbol{R}\_\Delta}
\end{equation}

其中$\Delta$表示坐标原点处原子的最近邻的原子。现在考虑一个简单**立方晶格**：

\begin{equation}
\begin{gathered}
\boldsymbol{R}\_\Delta=a(\pm1,0,0),\quad a(0,\pm1,0)\quad a(0,0,\pm1)\\\
\varepsilon\_n^\text{s.c.}(\boldsymbol{k})=T\_0^{(n)}+2\gamma\_n^{(1)}\left(\cos(k\_xa)+\cos(k\_ya)+\cos(k\_za\right)
\end{gathered}
\label{eq:112}
\end{equation}

这里$a$是晶格常数，$T\_0^{(n)}$和$\gamma\_n^{(1)}$是可由实验测定的参数。由对称性可知$\gamma\_n^{(1)}$为常数，其表达式为

\\[
\gamma\_n^{(1)}=\int\mathrm{d}\boldsymbol{r}\,\varphi\_n^\*(x,y,z)V\_1(x,y,z)\varphi\_n(x-a,y,z)
\\]

可由带宽$W$确定：

\begin{equation}
\label{eq:113}
W\_n^\text{s.c.}=12|\gamma\_n^{(1)}|
\end{equation}

由于带宽和重叠积分$\gamma$成正比，故紧束缚能带是窄带，能带间重叠越小，带宽越小。当能带重叠消失，带宽也消失，能带变成$N$重简并，和之前讨论的极限情况一致，那时电子束缚于$N$个独立的原子处。如[图 4](#fig-4)所示。

<figure id="fig-4">
  <img src="{{ '2018-03-27-many-body-model-systems-tight-binding.png' | prepend:'/upload/posts/' | relative_url }}" alt="tight binding band">
  <figcaption><b>图 4</b> 紧束缚能带示意图。</figcaption>
</figure>

除此之外\eqref{eq:112}所反映的简单立方晶格的能带特征也是紧束缚近似的一般特征。比如：

1.  当$ka$很小时，利用$\lim\_{x\to0}\cos x\sim1-\frac{1}{2}x^2$，\eqref{eq:112}成为  
\\[
\varepsilon\_n^\text{s.c.}(\boldsymbol{k})=T\_0^{(n)}+6\gamma\_n^{(1)}-\gamma\_n^{(1)}k^2a^2
\\]
与$\boldsymbol{k}$方向无关，即$\boldsymbol{k}=0$附近的等能面是个球面（这一特征可以推广到所有立方晶格的非简并能带）。带底在小$k$值附近是抛物线色散，这一点在凝胶模型中也适用。
2. 沿着任何一条垂直于第一布里渊区正方形表面所绘的$\varepsilon$色散曲线，在穿过该面时斜率为零。例如，沿着$k\_x$方向（此时$k\_y$和$k\_z$为常数），有  
\\[
\left.\frac{\partial}{\partial k\_x}\varepsilon\_n^\text{s.c.}(\boldsymbol{k})\right|\_{k\_x=\frac{\pi}{a}}=\left.-2a\gamma\_n^{(1)}\sin(k\_xa)\right|\_{k\_x=\frac{\pi}{a}}=0
\\]

严格来讲\eqref{eq:111}仅适用于$s$-带，对于$p$-，$d$-，$f$-……能带需要考虑更多的简并度，但这里我们点到为止，就不展开讲了。接下来的处理限制在$s$-带，顺便把$n$指标也去掉。

在二次量子化形式下，$H\_0$形如\eqref{eq:33}：

\begin{equation}
\label{eq:114}
H\_0=\sum\_{ij\sigma}T\_{ij}a\_{i\sigma}^\dagger a\_{j\sigma}
\end{equation}

紧束缚近似仅允许电子通过最近邻格点间的跃迁积分进行跃迁：

\begin{equation}
\label{eq:115}
T\_{ij}=\frac{1}{N\_\text{i}}\sum\_\boldsymbol{k}\varepsilon(\boldsymbol{k})e^{i\boldsymbol{k}\cdot(\boldsymbol{R}\_i-\boldsymbol{R}\_j)}
\end{equation}

带电子间的库伦相互作用\eqref{eq:56}自然仍然适用。转化到实空间便是

\begin{equation}
\label{eq:116}
H\_\text{ee}=\frac{1}{2}\sum\_{\substack{ijkl\\\ \sigma,\sigma'}}v(ij;kl)a\_{i\sigma}^\dagger a\_{j\sigma'}^\dagger a\_{l\sigma'}a\_{k\sigma}
\end{equation}

矩阵元通过原子波函数计算：

\begin{equation}
\label{eq:117}
v(ij;kl)=\frac{e^2}{4\pi\varepsilon\_0}\iint\mathrm{d}^3r\_1\,\mathrm{d}^3r\_2\,\frac{\varphi^\*(\boldsymbol{r}\_1-\boldsymbol{R}\_i)\varphi^\*(\boldsymbol{r}\_2-\boldsymbol{R}\_j)\varphi(\boldsymbol{r}\_2-\boldsymbol{R}\_l)\varphi(\boldsymbol{r}\_1-\boldsymbol{R}\_k)}{|\boldsymbol{r}\_1-\boldsymbol{r}\_2|}
\end{equation}

由于不同格点原子波函数的重叠积分很小，原子内的矩阵元

\begin{equation}
\label{eq:118}
U=v(ii;ii)
\end{equation}

起主导作用。Hubbard就建议干脆就把电子-电子相互作用限定在这一项：

> **Hubbard模型**：  
> \begin{equation}
\label{eq:119}
H=\sum\_{ij\sigma}T\_{ij}a\_{i\sigma}^\dagger a\_{j\sigma}+\frac{1}{2}U\sum\_{i,\sigma}\hat{n}\_{i\sigma}\hat{n}\_{i-\sigma}
\end{equation}

（注意：$\sigma=\uparrow(\downarrow)\iff-\sigma=\downarrow(\uparrow)$）。Hubbard模型必定是能让我们同时研究动能相互作用，库伦相互作用，泡利不相容原理以及晶格结构的最简单的模型，可谓小巧精悍。

为得到\eqref{eq:119}而用的大幅简化当然也给模型的使用带来局限性：

该模型用来讨论：
1. 窄能带固体的电子性质（例如，过渡金属），
2. 能带磁性，
3. 金属-绝缘体转变（“Mott转变”），
4. 统计力学的一般性原理，
5. 高温超导。

虽然结构简单，但Hubbard模型目前还没有精确解，还得借助各种近似来求解。接下来的部分用一些例子来讨论。

## 2 晶格振动
### 2.1 简谐近似
### 2.2 声子气

## 3 电子-声子相互作用
### 3.1 哈密顿量
### 3.2 有效电子-电子相互作用

## 4 自旋波
### 4.1 磁性固体分类
### 4.2 模型概念
### 4.3 磁子



