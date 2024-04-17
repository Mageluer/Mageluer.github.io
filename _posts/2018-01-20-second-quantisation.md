---
layout: post
title: 二次量子化
category: Science
tags: [Second quantisation, Quantum mechanics]
img: "2018-01-20-second-quantisation.png"
strip: "2018-01-20-second-quantisation-strip.png"
tex: true
toc: true
---

## 1 可分辨粒子
如果一个$N$粒子体系中粒子是可分辨的，基于量子力学的基本假定，可以对它们进行直接描述。首先，可以将诸粒子按照某种方式进行列举：
<mj>
\begin{equation}
\label{eq:1}
\{\mathcal{H}_1^{(i)};i=1,2,\cdots,N\}
\end{equation}
</mj>

其中<mj>$\mathcal{H}_1^{(i)}$</mj>是第$i$个粒子的希尔伯特空间。设<mj>$\{\widehat{\varphi}^{(i)}\}$</mj>构成空间<mj>$\mathcal{H}_1^{(i)}$</mj>中的一个ECOC（可对易算符的完全集合）；则（共同）本征矢<mj>$|\varphi_\alpha^{(i)}\rangle$</mj>构成<mj>$\mathcal{H}_1^{(i)}$</mj>的一组基。假定它们是正交的

<mj>
\begin{equation}
\label{eq:2}
\langle\varphi_\alpha^{(i)}|\varphi_\beta^{(i)}\rangle=\delta_{\alpha\beta}\qquad(\delta(\alpha-\beta))
\end{equation}
</mj>

$N$粒子体系的哈密顿空间是

<mj>
\begin{equation}
\label{eq:3}
\mathcal{H}_N=\mathcal{H}_1^{(1)}\otimes\mathcal{H}_1^{(2)}\otimes\cdots\otimes\mathcal{H}_1^{(N)},
\end{equation}
</mj>

其中$\mathcal{H}\_N$的基由相应单粒子基的直积构成

<mj>
\begin{align}
\begin{split}
|\varphi_N\rangle&=|\varphi_{\alpha_1}^{(1)}\varphi_{\alpha_2}^{(2)}\cdots\varphi_{\alpha_N}^{(N)}\rangle=\\
&=|\varphi_{\alpha_1}^{(1)}\rangle|\varphi_{\alpha_2}^{(2)}\rangle\cdots|\varphi_{\alpha_N}^{(N)}\rangle.
\end{split}
\label{eq:4}
\end{align}
</mj>

一般一个$N$粒子态<mj>$|\psi_N\rangle$</mj>可由<mj>$|\varphi_N\rangle$</mj>展开得到

<mj>
\begin{equation}
\label{eq:5}
|\psi_N\rangle=\sum_{\alpha_1,\ldots,\alpha_N}C(\alpha_1,\ldots,\alpha_N)|\varphi_{\alpha_1}^{(1)}\varphi_{\alpha_2}^{(2)}\cdots\varphi_{\alpha_N}^{(N)}\rangle
\end{equation}
</mj>

对这个$N$粒子态的统计解释和单粒子态一样，<mj>$|C(\alpha_1,\ldots,\alpha_N)|^2$</mj>是观察算符$\widehat{\varphi}$对<mj>$|\psi_N\rangle$</mj>测量得到<mj>$|\varphi_{\alpha_1}^{(1)}\cdots\varphi_{\alpha_N}^{(N)}\rangle$</mj>本征值的概率。运动方程可从原来的薛定谔方程导出：

<mj>
\begin{equation}
\label{eq:6}
i\hbar|\dot{\psi}_N\rangle=\widehat{H}|\psi_N\rangle
\end{equation}
</mj>

此处$\widehat{H}$是$N$粒子系统的哈密顿量。

量子力学处理可分辨粒子的多体系统的难度与经典物理相当，这是因为相对于单体问题来说，其复杂性大大提高。但是，全同粒子系统中的情况却有所不同。

## 2 全同粒子
### 2.1 全同粒子的定义
如果两个粒子的一切固有（内禀）属性（质量、自旋、电荷等等）完全一样，就说这两个粒子是全同的；任何实验都无法使一个粒子比另一个显得更特殊。此即不可分辨性。

从这个定义可见：若一个体系含有两个全同粒子，假如将它们互换，则体系性质及演化规律都不会产生任何变化。

> **附注**：  
> 必须注意，上面的定义和体系所处的实验条件无关；在一个特定实验中，即使我们并不测量粒子的电荷，也绝不能把电子和正电子当作全同粒子对待。

### 2.2 经典力学中的全同粒子
经典力学中的全同粒子尽管其物理性质全同，但并不失去其个性，故总可以通过一些手段加以鉴别。其原因是：
1. 经典粒子具有精确的局域性，比如具有精确的运动轨迹；
2. 经典粒子可供描述的特征是无限的，比如可以通过染色，加标签等方式区分；

例如，考虑以下两个全同粒子的体系。初始时刻<mj>$t_0$</mj>体系的物理状态由两粒子的位置及速度的数据描述；将这些数据记作<mj>$\{\mathbf{r}_0,\mathbf{v}_0\}$</mj>和<mj>$\{\mathbf{r}_0',\mathbf{v}_0'\}$</mj>。为描述该体系物理状态并研究其演变，给这两个粒子编号：<mj>$\{\mathbf{r}_1(t),\mathbf{v}_1(t)\}$</mj>表示粒子1在$t$时刻的位置和速度；<mj>$\{\mathbf{r}_2(t),\mathbf{v}_2(t)\}$</mj>表示粒子2在$t$时刻的位置和速度。这种编号本身与两粒子的物理性质并没有什么关系。由此，我们可以主观地用两个“数学态”来表述上述初态，令

<mj>
\begin{align}
\begin{split}
\{\mathbf{r}_1(t_0),\mathbf{v}_1(t_0)\}&=\{\mathbf{r}_0,\mathbf{v}_0\},\\
\{\mathbf{r}_2(t_0),\mathbf{v}_2(t_0)\}&=\{\mathbf{r}_0',\mathbf{v}_0'\},
\end{split}
\label{eq:7}
\end{align}
</mj>

或者相反

<mj>
\begin{align}
\begin{split}
\{\mathbf{r}_1(t_0),\mathbf{v}_1(t_0)\}&=\{\mathbf{r}_0',\mathbf{v}_0'\},\\
\{\mathbf{r}_2(t_0),\mathbf{v}_2(t_0)\}&=\{\mathbf{r}_0,\mathbf{v}_0\}.
\end{split}
\label{eq:8}
\end{align}
</mj>

现在来考虑体系的演变，假设初始条件\eqref{eq:7}所确定的运动方程的解可写作：

<mj>
\begin{equation}
\label{eq:9}
\mathbf{r}_1(t)=\mathbf{r}(t)\quad\mathbf{r}_2(t)=\mathbf{r}'(t)
\end{equation}
</mj>

全同性意味着，如果对换这两个粒子，这个体系不会发生任何改变，即拉格朗日函数和哈密顿函数不会变。由此可见，对应于初态\eqref{eq:8}的运动方程的解一定是：

<mj>
\begin{equation}
\label{eq:10}
\mathbf{r}_1(t)=\mathbf{r}'(t)\quad\mathbf{r}_2(t)=\mathbf{r}(t)
\end{equation}
</mj>

此处的$\mathbf{r}(t)$与$\mathbf{r}(t)'$和\eqref{eq:9}式相同。

于是，对该体系的这两种数学表述是完全等价的，因为它们导致相同的物理预言：于<mj>$t_0$</mj>时刻，从<mj>$\{\mathbf{r}_0,\mathbf{v}_0\}$</mj>出发的粒子在$t$时刻状态为<mj>$\{\mathbf{r}(t),\mathbf{v}(t)\}$</mj>，而从<mj>$\{\mathbf{r}_0',\mathbf{v}_0'\}$</mj>出发的粒子于$t$时刻则是<mj>$\{\mathbf{r}'(t),\mathbf{v}'(t)\}$</mj>。即

<mj>
\begin{align}
\label{eq:11}
\begin{split}
\{\mathbf{r}_0,\mathbf{v}_0\}&\longleftrightarrow\{\mathbf{r}(t),\mathbf{v}(t)\},\\
\{\mathbf{r}_0',\mathbf{v}_0'\}&\longleftrightarrow\{\mathbf{r}'(t),\mathbf{v}'(t)\}
\end{split}
\end{align}
</mj>

此条件下，只需要选择初始时刻的两种“数学态”中的一种；也就是说这样处理这个体系，似乎这两个粒子性质并不相同。在<mj>$t_0$</mj>时刻给这两个粒子任意标上号码(1)和(2)随后就变为据以区分这两个粒子的固有属性；这是因为我们可以沿着运动轨道逐点跟踪每一个粒子。

### 2.3 量子力学中的全同粒子
量子力学中的情况则完全不同，量子力学中全同粒子遵从不可分辨性原理。由于不确定性原理，电子的轨道概念不再具有任何含义。即使在初始时刻<mj>$t_0$</mj>，与两个全同粒子相关联的波包在空间是完全分开的，在此后的演变中它们也会相互交叠；于是就“失去粒子的踪迹”，因为在两个粒子出现概率都不为零的空间区域去探测一个粒子，是无法确知所探测到的粒子是号码为(1)的那个还是号码为(2)的那个。除了一些特殊情况（例如两个波包永不交叠）以外，测量两个粒子位置时它们的号码是含混不清的；实际上，从初态到达测量中观察到的态，其间存在很多不同的“道路”。概括而言，量子力学中的全同粒子完全不可分辨性来自于：
1. 粒子状态用波函数描述，只能确定其出现在某处的概率，不再有精确的局域性；
2. 单个粒子的状态是由相容算符的本征值来标志的，而相容算符的完全集是有限的；

例如，设想两个全同粒子在它们的质心坐标系内的碰撞。碰撞以前两个分开的波包相向而行，此时不妨约定一个粒子编号为(1)另一个为(2)；碰撞中两波包重叠；碰撞后两粒子出现的概率不为零的空间区域以球壳状扩大。设想一个探测器D于某个方向探测到一个粒子，由动量守恒律可知另一个粒子必然沿相反方向离去。但已无法知道探测器D所探测到的粒子是原来编号为(1)的粒子还是编号为(2)的粒子；于是从初态到观测时的末态，就有两种“道路”，分别对应编号为(1)的粒子被探测到（记作a道路）和编号为(2)的粒子被探测到（记作b道路）。现在便出现了一个基本的困难。为了计算一个测量结果出现的概率，我们需要知道与此测量结果相关的末态的态矢量。现在，可以写出两个态矢量，分别对应a道路和b道路。这两个右矢是不同的（却可以是正交的），但它们与同一个物理状态相联系，因为无法设想出一个更完善的测量方法来区分它们。这种情况下为了计算概率，应该选择a道路还是b道路呢？也许还可以设想同时考虑体系遵循两种可能的道路；若是这样，应该是把对应于两种道路的概率相加还是概率幅相加（这时又该带什么符号）？很容易看出（下面将证明），不同的可能性将导致不同的物理预言。

这种不可分辨性意味着物理相关量不因我们对粒子的排序改变而改变，此处的物理相关量就是指物理系统的可观测量。注意，物理可观测量不是指单独的算符或者态矢，而是指算符的期望值和态矢的点积。在$N$个粒子体系中，任何两个粒子互换顺序都不会引起这些量的变化，否则便可作为区分粒子的观测手段。于是我们有如下全同粒子体系的定义式：

<mj>
\begin{align}
\begin{split}
&\langle\varphi_{\alpha_1}^{(1)}\cdots\varphi_{\alpha_i}^{(i)}\cdots\varphi_{\alpha_j}^{(j)}\cdots\varphi_{\alpha_N}^{(N)}|\widehat{A}|\varphi_{\alpha_1}^{(1)}\cdots\varphi_{\alpha_i}^{(i)}\cdots\varphi_{\alpha_j}^{(j)}\cdots\varphi_{\alpha_N}^{(N)}\rangle\equiv\\\
\equiv&\langle\varphi_{\alpha_1}^{(1)}\cdots\varphi_{\alpha_i}^{(j)}\cdots\varphi_{\alpha_j}^{(i)}\cdots\varphi_{\alpha_N}^{(N)}|\widehat{A}|\varphi_{\alpha_1}^{(1)}\cdots\varphi_{\alpha_i}^{(j)}\cdots\varphi_{\alpha_j}^{(i)}\cdots\varphi_{\alpha_N}^{(N)}\rangle
\end{split}
\label{eq:12}
\end{align}
</mj>

这里下标$\alpha\_i$是态指标，上标$(i)$是粒子指标，$\widehat{A}$是任意观察算符。自然，上式不仅对$(i,j)$的所有组合成立，而且对粒子指标的所有置换都成立，因为任意置换都可以写成一系列位调操作。

### 2.4 交换简并
前面例子中所考察的两个波包最初是分开的，因此我们可以给它们中每一个任意标记号码(1)和(2)，但当需要确定与位置测量中某一给定结果相关联的数学右矢时，就出现了含混之处。实际上，为了选择一个数学右矢去描述初态，也会遇到同样的困难。这种类型的困难是与“交换简并”这一概念相联系的。

#### 2.4.1 交换简并的概念
以两全同粒子体系的数学描述为例，该体系可用单粒子态矢的张量积来表示

<mj>
\begin{equation}
\label{eq:13}
|k',k^{\prime\prime}\rangle\equiv|k'\rangle\otimes|k^{\prime\prime}\rangle\equiv|k'\rangle|k^{\prime\prime}\rangle
\end{equation}
</mj>

式中，指标$k'$和$k^{\prime\prime}$分别表示粒子1和粒子2的本征值集合（注意：<mj>$|k'\rangle|k^{\prime\prime}\rangle\equiv|k'\rangle_{(1)}|k^{\prime\prime}\rangle_{(2)}$</mj>）。同样

<mj>
\begin{equation}
\label{eq:14}
|k^{\prime\prime},k'\rangle\equiv|k^{\prime\prime}\rangle\otimes|k'\rangle\equiv|k^{\prime\prime}\rangle|k'\rangle
\end{equation}
</mj>

表示的两全同粒子体系的状态中，粒子1和粒子2的本征值集合由集体指标$k^{\prime\prime}$和$k'$表示。

当$k'\neq k^{\prime\prime}$时

<mj>
\begin{equation}
\label{eq:15}
\langle k^{\prime\prime},k'|k',k^{\prime\prime}\rangle=(\langle k^{\prime\prime}|k'\rangle)(\langle k'|k^{\prime\prime}\rangle)=0
\end{equation}
</mj>

这两个具有不同本征值集合的全同粒子态矢是互相正交的。

假设两全同粒子处于状态

<mj>
\begin{equation}
\label{eq:16}
|\alpha\rangle=c_1|k'\rangle|k^{\prime\prime}\rangle+c_2|k^{\prime\prime}\rangle|k'\rangle
\end{equation}
</mj>

式中，$k'$和$k^{\prime\prime}$是作用在第$i$个粒子态$\|k\rangle\_{(i)}$上的单粒子观察算符$\widehat{O}\_{(i)}$的本征值：

<mj>
\begin{equation}
\label{eq:17}
\widehat{O}_{(i)}|k\rangle_{(i)}=k|k\rangle_{(i)}
\end{equation}
</mj>

对于两全同粒子系统，有

<mj>
\begin{equation}
\label{eq:18}
(\widehat{O}_{(1)}\widehat{O}_{(2)})\left(c_1|k'\rangle|k^{\prime\prime}\rangle+c_2|k^{\prime\prime}\rangle|k'\rangle\right)=(k'k^{\prime\prime})\left(c_1|k'\rangle|k^{\prime\prime}\rangle+c_2|k^{\prime\prime}\rangle|k'\rangle\right)
\end{equation}
</mj>

可见，测量结果对于$k'\leftrightarrow k^{\prime\prime}$不变，此即所谓交换简并。

#### 2.4.2 两个自旋$1/2$的体系的交换简并
假设体系有两个自旋为$1/2$的全同粒子，只讨论它们的自旋自由度。注意要区别体系的物理状态和对状态的数学描述（即态空间中的右矢）。似乎可以很自然地设想，对每个自旋进行完全的测量就能确知总体系的物理状态。下面假设一个自旋为$Oz$方向的分量为$+\hbar/2$，另一个为$-\hbar/2$。为了从数学上描述这个体系，给粒子编号：$\widehat{S}\_1$和$\widehat{S}\_2$表示两个观察算符，在态空间中，由$\widehat{S}\_{1z}$（本征值为$\varepsilon\_1\hbar/2$）和$\widehat{S}\_{2z}$（本征值为$\varepsilon\_2\hbar/2$）的共同本征右矢组成的正交归一基为<mj>$\{|\varepsilon_1,\varepsilon_2\rangle\}$</mj>（$\varepsilon\_1$和$\varepsilon\_2$可以取$+$和$-$）。

和在经典力学中的情形一样，可以有两个不同的“数学态”和同一个物理态相联系；这里我们可以用以下两个正交右矢中的任何一个来描述所要考察的物理态：

<mj>
\begin{align}
&\label{eq:19}|\varepsilon_1=+,\varepsilon_2=-\rangle,\\
&\label{eq:20}|\varepsilon_1=-,\varepsilon_2=+\rangle.
\end{align}
</mj>

这两个右矢张成一个二维子空间，其中归一化矢量具有下列形式：

<mj>
\begin{equation}
\label{eq:21}
\alpha|+,-\rangle+\beta|-,+\rangle
\end{equation}
</mj>

并附以下列条件

<mj>
\begin{equation}
\label{eq:22}
|\alpha|^2+|\beta|^2=1
\end{equation}
</mj>

按照叠加原理，所有的数学右矢\eqref{eq:21}都可以表示同一个物理态如\eqref{eq:19}或\eqref{eq:20}。于是这里存在着一种交换简并。

交换简并引起了基本的困难，因为不同的右矢\eqref{eq:21}会导致依赖于所选择的右矢的物理预言。例如，求发现两个自旋沿$Ox$轴分量都等于$+\hbar/2$的概率。与这个测量联系着自旋态空间中唯一的一个右矢。$S\_x$的本征矢$\|\pm\rangle\_x$在$S\_z$的本征矢$\|\pm\rangle$所构成的基可展开为

<mj>
\begin{equation}
\label{eq:23}
|\pm\rangle_x=\frac{1}{\sqrt{2}}\left[|+\rangle\pm|-\rangle\right].
\end{equation}
</mj>

这样，这个右矢可以写作：

<mj>
\begin{align}
\label{eq:24}
\begin{split}
&\frac{1}{\sqrt{2}}[|\varepsilon_1=+\rangle+|\varepsilon_1=-\rangle]\otimes
\frac{1}{\sqrt{2}}[|\varepsilon_2=+\rangle+|\varepsilon_2=-\rangle]=\\
=&\frac{1}{2}[|+,+\rangle+|-,+\rangle+|+,-\rangle+|-,-\rangle]
\end{split}
\end{align}
</mj>

因此，对于\eqref{eq:21}中的矢量，待求的概率为

<mj>
\begin{equation}
\label{eq:25}
\left|\frac{1}{2}(\alpha+\beta)\right|^2
\end{equation}
</mj>

这个概率依赖于系数$\alpha$和$\beta$。由此可见，不能企图用右矢集合\eqref{eq:21}或任意选自其中一个的右矢来描述所要考察的物理态。必须消除交换简并；这就是说，必须毫不含糊地指明，究竟使用\eqref{eq:21}中的哪一个右矢。

> **附注**：  
> 在上面的例子里，交换简并只出现在初态，这是因为已将末态中的两个自旋分量取为同一个数值。在一般情况下（例如，测量结果对应于$S\_x$的两个互异本征值），交换简并应同时出现在初态和末态）。

#### 2.4.3 推广
研究含有$N$个（$N>1$）全同粒子的任何体系，都会遇到交换简并所带来的困难。以三粒子体系为例，孤立地考察三个粒子中的每一个，各自都联系着一个态空间和在此空间起作用的观察算符。于是将这些粒子编号：$\mathcal{H}^{(1)}$、$\mathcal{H}^{(2)}$、$\mathcal{H}^{(3)}$表示三个单粒子的态空间，对应的诸观察算符可标以同样的下标。三粒子的态空间是以下张量积：

\begin{equation}
\label{eq:26}
\mathcal{H}=\mathcal{H}^{(1)}\otimes\mathcal{H}^{(2)}\otimes\mathcal{H}^{(3)}
\end{equation}

现在来考虑最初定义在空间$\mathcal{H}^{(1)}$中的观察算符$\widehat{B}^{(1)}$。假设$\widehat{B}^{(1)}$本身就构成空间$\mathcal{H}^{(1)}$中的一个ECOC[或设$\widehat{B}^{(1)}$是构成ECOC的一组算符]。三个粒子是相同的，意味着观察算符$\widehat{B}^{(2)}$，$\widehat{B}^{(3)}$都存在，且分别在$\mathcal{H}^{(2)}$和$\mathcal{H}^{(3)}$中构成ECOC。$\widehat{B}^{(1)}$，$\widehat{B}^{(2)}$和$\widehat{B}^{(3)}$具有相同的谱$\\{b\_n;n=1,2,\cdots\\}$。利用这三个观察算符在空间$\mathcal{H}^{(1)}$，$\mathcal{H}^{(2)}$及$\mathcal{H}^{(3)}$中确定的基，通过张量积，就可以构成空间$\mathcal{H}$中的一个正交归一基，记作：

<mj>
\begin{equation}
\label{eq:27}
\{|1:b_i;2:b_j;3:b_k\rangle;i,j,k=1,2,\cdots\}
\end{equation}
</mj>

诸右矢<mj>$|1:b_i;2:b_j;3:b_k\rangle$</mj>都是$\widehat{B}^{(1)}$，$\widehat{B}^{(2)}$和$\widehat{B}^{(3)}$在空间$\mathcal{H}$中的延伸算符的共同本征矢，属于各自对应的本征值<mj>$b_i,b_j,b_k$</mj>。

全同性使我们不能测量到$\widehat{B}^{(1)}$或$\widehat{B}^{(2)}$或$\widehat{B}^{(3)}$，这是因为编号没有任何物理根据；但可以去对三个粒子中的每一个去测物理量$\widehat{B}$。假定测得的结果是三个互异本征值<mj>$b_n,b_p,b_q$</mj>。现在就会出现交换简并了，因为可以主观使用由空间$\mathcal{H}$中的下列六个基矢量：

<mj>
\begin{align}
\label{eq:28}
\begin{split}
&|1:b_n;2:b_p;3:b_q\rangle,|1:q_n;2:b_n;3:b_p\rangle,|1:b_p;2:b_q;3:b_n\rangle,\\
&|1:b_n;2:b_q;3:b_p\rangle,|1:p_n;2:b_n;3:b_q\rangle,|1:b_q;2:b_p;3:b_n\rangle
\end{split}
\end{align}
</mj>

所张成的子空间中的任何一个右矢来表示体系在测量之后的态。可见，针对每一个粒子完全测量并不能在体系的态空间中确定一个唯一的右矢。

> **附注**：  
> 如果测量所得本征值中有两个是相等的，那么由交换简并引起的不确定性就不是很重要了；在三个测量结果相等的特殊情况下，这种不确定性甚至消失了。

## 3 置换算符
现在暂不陈述可以消除交换简并引起的不确定性的补充假定，先来研究一些算符，它们被定义在所要考察的体系的总态空间中，而它们的作用不过是对换该体系中的诸粒子。

### 3.1 位调算符$P\_{ij}$
位调算符$P\_{ij}$是这样一个线性算符，它对基矢的作用如下：

<mj>
\begin{align}
\label{eq:29}
\begin{split}
P_{ij}|\cdots\varphi_{\alpha_i}^{(i)}\cdots\varphi_{\alpha_j}^{(j)}\cdots\rangle=&|\cdots\varphi_{\alpha_i}^{(j)}\cdots\varphi_{\alpha_j}^{(i)}\cdots\rangle=\\
=&|\cdots\varphi_{\alpha_j}^{(i)}\cdots\varphi_{\alpha_i}^{(j)}\cdots\rangle
\end{split}
\end{align}
</mj>

下面来讨论位调算符的一些性质。当我们把$P\_{ij}$在$N$粒子态上作用两次又回到这个态，这意味着

<mj>
\begin{equation}
\label{eq:30}
P_{ij}^2=\mathbf{1}\iff P_{ij}=P_{ij}^{-1}
\end{equation}
</mj>

式\eqref{eq:12}可写成以下形式：

<mj>
\begin{equation}
\label{eq:31}
\langle\varphi_N|\widehat{A}|\varphi_N\rangle\equiv\langle P_{ij}\varphi_N|\widehat{A}|P_{ij}\varphi_N\rangle=\langle\varphi_N|P_{ij}^\dagger\widehat{A}P_{ij}|\varphi_N\rangle
\end{equation}
</mj>

上式对$\mathcal{H}\_N$的任意$N$粒子态都成立；进一步，对任意矩阵元$\langle\varphi\_N\|\widehat{A}\|\psi\_N\rangle$也成立，因为我们总能够将其做如下分解

<mj>
\begin{align}
\label{eq:32}
\begin{split}
\langle\varphi_N|\widehat{A}|\psi_N\rangle=&\frac{1}{4}\left\{\langle\varphi_N+\psi_N|\widehat{A}|\varphi_N+\psi_N\rangle\right.\\
&-\langle\varphi_N-\psi_N|\widehat{A}|\varphi_N-\psi_N\rangle\\
&+i\langle\varphi_N-i\psi_N|\widehat{A}|\varphi_N-i\psi_N\rangle\\
&\left.-i\langle\varphi_N+i\psi_N|\widehat{A}|\varphi_N+i\psi_N\rangle\right\}
\end{split}
\end{align}
</mj>

由此得到如下算符恒等式：

<mj>
\begin{equation}
\label{eq:33}
\widehat{A}=P_{ij}^{\dagger}\widehat{A}P_{ij},\quad\forall(i,j)
\end{equation}
</mj>
当上式中$\widehat{A}=\mathbf{1}$，便得到

<mj>
\begin{equation}
\label{eq:34}
\mathbf{1}=P_{ij}^\dagger P_{ij}\quad\Rightarrow P_{ij}=P_{ij}^\dagger P_{ij}^2=P_{ij}^\dagger
\end{equation}
</mj>

实际上，算符$P\_{ij}$在基<mj>$|\cdots\varphi_{\alpha_i}^{(i)}\cdots\varphi_{\alpha_j}^{(j)}\cdots\rangle$</mj>中的矩阵元可写作

<mj>
\begin{align}
\label{eq:35}
\begin{split}
&\langle\cdots\varphi_{\alpha_{i'}}^{(i)}\cdots\varphi_{\alpha_{j'}}^{(j)}\cdots|P_{ij}|\cdots\varphi_{\alpha_i}^{(i)}\cdots\varphi_{\alpha_j}^{(j)}\cdots\rangle=\\
=&\langle\cdots\varphi_{\alpha_{i'}}^{(i)}\cdots\varphi_{\alpha_{j'}}^{(j)}\cdots|\cdots\varphi_{\alpha_j}^{(i)}\cdots\varphi_{\alpha_i}^{(j)}\cdots\rangle=\\
=&\delta_{i'j}\delta_{j'i}
\end{split}
\end{align}
</mj>

按照定义，算符$P\_{ij}^\dagger$的矩阵元为：

<mj>
\begin{align}
\label{eq:36}
\begin{split}
&\langle\cdots\varphi_{\alpha_{i'}}^{(i)}\cdots\varphi_{\alpha_{j'}}^{(j)}\cdots|P_{ij}^\dagger|\cdots\varphi_{\alpha_i}^{(i)}\cdots\varphi_{\alpha_j}^{(j)}\cdots\rangle=\\
=&\left(\langle\cdots\varphi_{\alpha_i}^{(i)}\cdots\varphi_{\alpha_j}^{(j)}\cdots|P_{ij}|\cdots\varphi_{\alpha_{i'}}^{(i)}\cdots\varphi_{\alpha_{j'}}^{(j)}\cdots\rangle\right)^*=\\
=&\left(\langle\cdots\varphi_{\alpha_i}^{(i)}\cdots\varphi_{\alpha_j}^{(j)}\cdots|\cdots\varphi_{\alpha_{j'}}^{(i)}\cdots\varphi_{\alpha_{i'}}^{(j)}\cdots\rangle\right)^*=\\
=&\delta_{ij'}\delta_{ji'}
\end{split}
\end{align}
</mj>

于是，$P\_{ij}$的每个矩阵元都等于$P\_{ij}^\dagger$的对应矩阵元，同样证明了\eqref{eq:34}式。

由此可见全同粒子态空间$\mathcal{H}\_N$中的位调算符$P\_{ij}$是厄密且幺正的：

<mj>
\begin{equation}
\label{eq:37}
P_{ij}=P_{ij}^\dagger=P_{ij}^{-1}
\end{equation}
</mj>

从\eqref{eq:33}也能发现

<mj>
\begin{equation}
\label{eq:38}
P_{ij}\widehat{A}=P_{ij}P_{ij}^\dagger\widehat{A}P_{ij}=\widehat{A}P_{ij}.
\end{equation}
</mj>

即$N$粒子体系的观察算符与位调算符$P\_{ij}$对易：

<mj>
\begin{equation}
\label{eq:39}
[P_{ij},\widehat{A}]_-=P_{ij}\widehat{A}-\widehat{A}P_{ij}=0
\end{equation}
</mj>

当然，对于哈密顿算符$\widehat{H}$上式也成立

<mj>
\begin{equation}
\label{eq:40}
[P_{ij},\widehat{H}]_-=0
\end{equation}
</mj>

对全同粒子体系的观察算符的一个必要但显而易见的要求是，它们明确的依赖于所有这$N$个粒子的指标（比如坐标）。实际上，考虑一个观察算符$\widehat{\varphi}^{(i)}$，它原是定义在空间$\mathcal{H}^{(i)}$中的，然后延伸至空间$\mathcal{H}$。总可以用$\widehat{\varphi}^{(i)}$的一组本征矢构成空间$\mathcal{H}^{(i)}$中的基$\\{\|\varphi\_{\alpha\_i}\rangle\\}$（对应的本征值记作$\varphi\_{\alpha\_i}$）。考虑算符$P\_{ij}\widehat{\varphi}^{(i)}P\_{ij}^\dagger$对空间$\mathcal{H}$中的任意基右矢的作用：

<mj>
\begin{align}
\label{eq:41}
\begin{split}
P_{ij}\widehat{\varphi}^{(i)}P_{ij}^\dagger|\cdots\varphi_{\alpha_i}^{(i)}\cdots\varphi_{\alpha_j}^{(j)}\cdots\rangle=&P_{ij}\widehat{\varphi}^{(i)}|\cdots\varphi_{\alpha_j}^{(i)}\cdots\varphi_{\alpha_i}^{(j)}\cdots\rangle=\\
=&\varphi_{\alpha_j}P_{ij}|\cdots\varphi_{\alpha_j}^{(i)}\cdots\varphi_{\alpha_i}^{(j)}\cdots\rangle=\\
=&\varphi_{\alpha_j}|\cdots\varphi_{\alpha_i}^{(i)}\cdots\varphi_{\alpha_j}^{(j)}\cdots\rangle
\end{split}
\end{align}
</mj>

这相当于将观察算符$\widehat{\varphi}^{(j)}$直接作用于基右矢，因而有：

<mj>
\begin{equation}
\label{eq:42}
P_{ij}\widehat{\varphi}^{(i)}P_{ij}^\dagger=\widehat{\varphi}^{(j)}
\end{equation}
</mj>

可见位调算符改变了观察算符作用的粒子的标记。

在空间$\mathcal{H}$中还存在一些观察算符，诸如$\widehat{\varphi}^{(i)}+\widehat{\psi}^{(j)}$或$\widehat{\varphi}^{(i)}\widehat{\psi}^{(j)}$，它们都同时涉及两个指标。显然有：

<mj>
\begin{equation}
\label{eq:43}
P_{ij}[\widehat{\varphi}^{(i)}+\widehat{\psi}^{(j)}]P_{ij}^\dagger=\widehat{\varphi}^{(j)}+\widehat{\psi}^{(i)}
\end{equation}
</mj>

利用式\eqref{eq:34}还可以得到：

<mj>
\begin{align}
\label{eq:44}
\begin{split}
P_{ij}\widehat{\varphi}^{(i)}\widehat{\psi}^{(j)}P_{ij}^\dagger=&P_{ij}\widehat{\varphi}^{(i)}P_{ij}^\dagger P_{ij}\widehat{\psi}^{(j)}P_{ij}^\dagger=\\
=&\widehat{\varphi}^{(j)}\widehat{\psi}^{(i)}
\end{split}
\end{align}
</mj>

这些结果可以推广到$\mathcal{H}$中所有可以表示为$\widehat{\varphi}^{(i)}$和$\widehat{\psi}^{(j)}$的函数的观察算符，将这类算符记作$\widehat{O}^{(i,j)}$，便有：

<mj>
\begin{equation}
\label{eq:45}
P_{ij}\widehat{O}^{(i,j)}P_{ij}^\dagger=\widehat{O}^{(j,i)}
\end{equation}
</mj>

这里的$\widehat{O}^{(j,i)}$是将$\widehat{O}^{(i,j)}$各处指标$i$和$j$都交换得到的观察算符。

若一个观察算符$\widehat{O}\_S^{(i,j)}$满足：

<mj>
\begin{equation}
\label{eq:46}
\widehat{O}_S^{(i,j)}=\widehat{O}_S^{(j,i)}
\end{equation}
</mj>

便说它们是对称的。由式\eqref{eq:45}可见

<mj>
\begin{equation}
\label{eq:47}
P_{ij}\widehat{O}_S^{(i,j)}=\widehat{O}_S^{(i,j)}P_{ij}
\end{equation}
</mj>

即

<mj>
\begin{equation}
\label{eq:48}
[P_{ij},\widehat{O}_S^{(i,j)}]_-=0
\end{equation}
</mj>

由此可以看出全同粒子体系的观察算符所要满足的条件是，依赖于所有这$N$个粒子的指标的对称算符。

全同粒子的不可分辨性原理说明位调算符对$N$粒子态的作用仅仅是增加一个相位因子；特别地，$\|\varphi\_N\rangle$必然是$P\_{ij}$的一个本征态：

<mj>
\begin{align}
\label{eq:49}
\begin{split}
P_{ij}|\cdots\varphi_{\alpha_i}^{(i)}\cdots\varphi_{\alpha_j}^{(j)}\cdots\rangle&=|\cdots\varphi_{\alpha_i}^{(j)}\cdots\varphi_{\alpha_j}^{(i)}\cdots\rangle=\\
&=\lambda|\cdots\varphi_{\alpha_i}^{(i)}\cdots\varphi_{\alpha_j}^{(j)}\cdots\rangle
\end{split}
\end{align}
</mj>

从\eqref{eq:30}及\eqref{eq:34}看来，$P\_{ij}$只有两个实本征值：

\begin{equation}
\label{eq:50}
\lambda=\pm1
\end{equation}

这与$(i,j)$对儿的选择无关，由此得到这样的结论：位调算符$P\_{ij}$的本征矢分为对称右矢（$\lambda=+1$）和反对称右矢（$\lambda=-1$），即

<mj>
\begin{align}
P_{ij}|\psi_N^{(+)}\rangle&=|\psi_N^{(+)}\rangle\quad\forall(i,j)\Rightarrow|\psi_N^{(+)}\rangle\quad\text{symmetric state}\label{eq:51}\\
P_{ij}|\psi_N^{(-)}\rangle&=-|\psi_N^{(-)}\rangle\quad\forall(i,j)\Rightarrow|\psi_N^{(-)}\rangle\quad\text{antisymmetric state}\label{eq:52}\\
\end{align}
</mj>

对于时间演化算符

<mj>
\begin{equation}
\label{eq:53}
U(t,t_0)=\exp\left(-\frac{i}{\hbar}H(t-t_0)\right),\quad H\neq H(t)
\end{equation}
</mj>

由\eqref{eq:40}可见：

<mj>
\begin{equation}
\label{eq:54}
[P_{ij},U]_-=0
\end{equation}
</mj>

这意味着全同粒子的右矢的对称（反对称）性会一直保持。

### 3.2 置换算符$\mathcal{P}$
#### 3.2.1 定义
置换算符是这样定义：

<mj>
\begin{equation}
\label{eq:55}
\mathcal{P}|\varphi_{\alpha_1}^{(1)}\varphi_{\alpha_2}^{(2)}\cdots\varphi_{\alpha_N}^{(N)}\rangle=|\varphi_{\alpha_1}^{(i_1)}\varphi_{\alpha_2}^{(i_2)}\cdots\varphi_{\alpha_N}^{(i_N)}\rangle
\end{equation}
</mj>

这里的$\mathcal{P}$是作用在粒子指标上的，当然也可以使其作用在态指标$\alpha\_i$上。$(i\_1,i\_2,\cdots,i\_N)$是由$N$元组$(1,2,\cdots,N)$置换得到的。对于$N$个全同粒子的体系，可以此方法定义$N!$个置换算符。

#### 3.2.2 性质
1. 置换算符的集合构成一个群，它是对称群的子群。
2. 每一个置换算符都可以分解为位调算符的乘积。这种分解不唯一，但其中位调算符的个数的宇称是不变的。实际上$S\_n\rightarrow\\{-1,+1\\}$是一个群同态，同态核是$n$次交错群。置换算符的伴随算符具有和前者一样的宇称，因为这相当于同等数目的位调算符按照相反顺序相乘。
3. 置换算符是幺正的，因为它是若干幺正位调算符的乘积。但置换算符未必是厄密的，因为一般位调算符彼此并不对易。

#### 3.2.3 对称化算符
当$N>2$时，诸位调算符不可对易，无法用这些算符的本征矢构成一个基。但存在一些右矢，它们同时是所有置换算符的本征矢。下面以\eqref{eq:4}为出发点来构造这些右矢。

定义如下对称化算符：

<mj>
\begin{equation}
\label{eq:56}
\widehat{S}_\varepsilon=\sum_{\mathcal{P}}\varepsilon^p\mathcal{P}
\end{equation}
</mj>

其中$\varepsilon=\pm$，$p$是构成$\mathcal{P}$的位调算符的数目，上式对$N$元组$(1,2,\ldots,N)$的所有可能的置换$\mathcal{P}$进行求和。上式中的$\mathcal{P}$左乘位调算符$P\_{ij}$，根据重排定理，式中变成另一个置换算符$\mathcal{P}'$，且$p'=p\pm1$。

<mj>
\begin{equation}
\label{eq:57}
P_{ij}\widehat{S}_\varepsilon=\sum_{\mathcal{P}}\varepsilon^p P_{ij}\mathcal{P}=\sum_{\mathcal{P}}\varepsilon^p\mathcal{P}'=\varepsilon\sum_{\mathcal{P}'}\varepsilon^{p'}\mathcal{P}'
\end{equation}
</mj>

这意味着：

<mj>
\begin{equation}
\label{eq:58}
P_{ij}\widehat{S}_\varepsilon=\varepsilon\widehat{S}_\varepsilon
\end{equation}
</mj>

于是就能得到态空间$\mathcal{H}\_N$中完全对称化（反对称化）的子空间$\mathcal{H}^{(\pm)}$

<mj>
\begin{equation}
\label{eq:59}
|\psi_N^{(\varepsilon)}\rangle=\widehat{S}_\varepsilon|\psi_{\alpha_1}^{(1)}\psi_{\alpha_2}^{(2)}\cdots\psi_{\alpha_N}^{(N)}\rangle
\end{equation}
</mj>

满足式\eqref{eq:51}和式\eqref{eq:52}。

对于一个一般的置换算符$\mathcal{P}$，有如下关系式：

<mj>
\begin{equation}
\label{eq:60}
\mathcal{P}\widehat{S}_\varepsilon=\varepsilon^p\widehat{S}_\varepsilon\Longleftrightarrow\mathcal{P}|\psi_N^{(\varepsilon)}\rangle=\varepsilon^p|\psi_N^{(\varepsilon)}\rangle
\end{equation}
</mj>

## 4 对称化假定
### 4.1 假定的陈述
现在来陈述这样一个假定：  
在体系含有多个全同粒子时，只有其态空间的某些右矢才能描述其物理状态，根据全同粒子的性质，这些物理右矢，对粒子的对换而言，或是完全对称的，或是完全反对称的。称前者为玻色子，它们的物理右矢是对称的；后者为费米子，它们的物理右矢是反对称的。

由此可见，该对称化假定限制了全同粒子的态空间；和性质互异的粒子系相反，这个态空间不是组成各个粒子态空间的张量积$\mathcal{H}$，而仅仅是$\mathcal{H}$的一个子空间$\mathcal{H}^{(+)}$或$\mathcal{H}^{(-)}$，由粒子是玻色子或费米子而定。

按照“自旋统计理论”（此处不加证明地给出），自旋为半整数的粒子（电子、正电子、质子、中子，$\mu$子等）都是费米子，自旋为整数的粒子（光子，介子等）都是玻色子。

> **附注**：  
> 对所谓的“基本粒子”来说，这个规律一经证实，对于由这些粒子组成的其他粒子来说，它也就得到了证实。因为当我们对换全同的复合粒子时，相当于对换组成这些粒子的全体粒子，这些复合粒子的交换对称性（反对称性）便由它们总的自旋决定了。

### 4.2 交换简并的消除
[2.4](#24-交换简并)节中的讨论可以归结如下：假设右矢$\|\psi\rangle$可以从数学上描述$N$个全同粒子体系的一个完全确定的状态，那么在$\|\psi\rangle$及用置换算符对其变换得到的全体$\mathcal{P}\|\psi\rangle$所张成的子空间$\mathcal{H}\_\psi$中所有的右矢都可以描述那个物理状态。子空间维数可以从$1$到$N!$，由所选定的右矢$\|\psi\rangle$来确定。维数大于$1$时便有若干个数学右矢对应同一个物理态，就出现了交换简并。此时，仅仅用ECOC的本征值来描述不足以确定体系的状态。例如，从\eqref{eq:18}式可见，仅仅用ECOC的本征值不能确定两全同粒子体系状态$c\_1\|k'\rangle\|k^{\prime\prime}\rangle+c\_2\|k^{\prime\prime}\rangle\|k'\rangle$中组合系数的比值$c\_2/c\_1$。

上面引入的新假定严格限制了可以描述一个物理状态的数学右矢的种类：对于玻色子，这些右矢必须属于$\mathcal{H}^{(+)}$；对于费米子，它们必须属于$\mathcal{H}^{(-)}$。可以这样说，如果证明了空间$\mathcal{H}\_\psi$只含有$\mathcal{H}^{(+)}$中的一个右矢或$\mathcal{H}^{(-)}$中的一个右矢，那么交换简并带来的困难也就消除了。事实上，从\eqref{eq:60}式可见空间$\mathcal{H}\_\psi$中的全部右矢，在$\mathcal{H}^{(+)}$上或$\mathcal{H}^{(-)}$的投影都是共线的。于是对称化假设毫不含糊地（除常数因子以外）指明与所考察物理状态相联系的$\mathcal{H}\_\psi$中的那个右矢：对于玻色子，就是$\widehat{S}\_+\|\psi\rangle$；对于费米子，就是$\widehat{S}\_-\|\psi\rangle$。下面，称它们为物理右矢。

此处还要指出，具有混合对称性的全同粒子体系不可能存在。设想$\|\varphi\_N^{(\varepsilon)}\rangle$和$\|\psi\_N^{(\varepsilon')}\rangle$是$N$全同粒子系统的两个可能的态，那么有可能存在一个合适的算符，比如$\hat{x}$（或算符集合），使一个态转换到另一个。形式上，这意味着以下标量积

<mj>
\begin{equation}
\label{eq:61}
\langle\varphi\_N^{(\varepsilon)}|\hat{x}|\psi\_N^{(\varepsilon')}\rangle\neq0
\end{equation}
</mj>

进一步可见：

<mj>
\begin{align}
\label{eq:62}
\begin{split}
\varepsilon\langle\varphi_N^{(\varepsilon)}|\hat{x}|\psi_N^{(\varepsilon')}\rangle&=\langle P_{ij}\varphi_N^{(\varepsilon)}|\hat{x}|\psi_N^{(\varepsilon')}\rangle=\langle\varphi_N^{(\varepsilon)}|P_{ij}^\dagger\hat{x}|\psi_N^{(\varepsilon')}\rangle=\\\
&=\langle\varphi_N^{(\varepsilon)}|P_{ij}\hat{x}|\psi_N^{(\varepsilon')}\rangle=\langle\varphi_N^{(\varepsilon)}|\hat{x}P_{ij}|\psi_N^{(\varepsilon')}\rangle=\\\
&=\varepsilon'\langle\varphi_N^{(\varepsilon)}|\hat{x}|\psi_N^{(\varepsilon')}\rangle
\end{split}
\end{align}
</mj>

由此得到$\varepsilon=\varepsilon'$。

> **附注**：  
> 可能出现这种情况，空间$\mathcal{H}\_\psi$中的全部右矢在在$\mathcal{H}^{(+)}$上（或$\mathcal{H}^{(-)}$）上的投影都等于零。这种情况下，对应的物理状态就被排除在对称化假定之外。

### 4.3 物理右矢的构成
对于含有$N$个全同粒子的体系的一个给定的物理状态，可以由以下方式构造出，对应于该状态的唯一右矢（物理右矢）：
1. 任意给诸粒子编号，并构成与所考察的物理状态及已有的号码对应的右矢$\|\psi\rangle$。
2. 按照全同粒子是费米子还是玻色子，将$\widehat{S}\_+$或$\widehat{S}\_-$作用于右矢$\|\psi\rangle$。
3. 将所得右矢归一化。

全同费米子体系是完全反对称态，满足泡利不相容原理（没有两个电子可以占据同一个量子态），服从费米-狄拉克统计。全同玻色子是完全对称态，服从玻色-爱因斯坦统计，在极低温会发生玻色-爱因斯坦凝聚（全部粒子趋向于回到基态）。

这里举一个例子，考虑两“自由”电子体系（不考虑其相互作用）。其波函数$\|\psi\rangle$可分解为轨道波函数$\|\varphi\rangle$与自旋波函数$\|\chi\rangle$乘积。由于电子为费米子，$\|\psi\rangle$应当是反对称的。故而有两种情况：  
1. 当$\|\varphi\rangle$对称时，$\|\chi\rangle$反对称，对应自旋单态。
2. 当$\|\varphi\rangle$反对称时，$\|\chi\rangle$对称，对应自旋三重态。

于是有

<mj>
\begin{align}
|\psi^{(-)}\rangle&=|\varphi^{(+)}\chi^{(-)}\rangle\label{eq:63}\\
|\psi^{(-)}\rangle&=|\varphi^{(-)}\chi^{(+)}\rangle\label{eq:64}\\
\end{align}
</mj>

其中，$\|\varphi^{(\varepsilon)}\rangle$和$\|\chi^{(\varepsilon)}\rangle$分别按照上述步骤构成：

<mj>
\begin{align}
|\varphi^{(+)}\rangle&=\frac{1}{\sqrt{2}}\left(|\varphi\_{x_1}^{(1)}\varphi_{x_2}^{(2)}\rangle+|\varphi_{x_1}^{(2)}\varphi_{x_2}^{(1)}\rangle\right)\label{eq:65}\\
|\varphi^{(-)}\rangle&=\frac{1}{\sqrt{2}}\left(|\varphi_{x_1}^{(1)}\varphi_{x_2}^{(2)}\rangle-|\varphi_{x_1}^{(2)}\varphi_{x_2}^{(1)}\rangle\right)\label{eq:66}\\
\end{align}
</mj>

和

<mj>
\begin{align}
|\chi^{(+)}\rangle&=\begin{cases}
|++\rangle\\
\frac{1}{\sqrt{2}}(|+-\rangle+|-+\rangle)\\
|--\rangle
\end{cases}\label{eq:67}\\
|\chi^{(-)}\rangle&=\frac{1}{\sqrt{2}}(|+-\rangle-|-+\rangle)\label{eq:68}\\
\end{align}
</mj>

“自由”电子1出现在$\mathbf{x}\_1$附近的$\mathrm{d}^3x\_1$内且“自由”电子2出现在$\mathbf{x}\_2$附近的$\mathrm{d}^3x\_2$内的概率为

<mj>
\begin{align}
\begin{split}
&\langle\psi^{(-)}|\psi^{(-)}\rangle\mathrm{d}^3x_1\mathrm{d}^3x_2=\\
=&\frac{1}{2}\left(\langle\varphi_{x_1}^{(1)}\varphi_{x_2}^{(2)}|-\varepsilon\langle\varphi_{x_1}^{(2)}\varphi_{x_2}^{(1)}|\right)\left(|\varphi_{x_1}^{(1)}\varphi_{x_2}^{(2)}\rangle-\varepsilon|\varphi_{x_1}^{(2)}\varphi_{x_2}^{(1)}\rangle\right)\langle\chi^{(\varepsilon)}|\chi^{(\varepsilon)}\rangle\mathrm{d}^3x_1\mathrm{d}^3x_2=\\
=&\frac{1}{2}\left(\langle\varphi_{x_1}^{(1)}\varphi_{x_2}^{(2)}|\varphi_{x_1}^{(1)}\varphi_{x_2}^{(2)}\rangle+\varepsilon^2\langle\varphi_{x_1}^{(2)}\varphi_{x_2}^{(1)}|\varphi_{x_1}^{(2)}\varphi_{x_2}^{(1)}\rangle-\right.\\
&\left.-\varepsilon\langle\varphi_{x_1}^{(1)}\varphi_{x_2}^{(2)}|\varphi_{x_1}^{(2)}\varphi_{x_2}^{(1)}\rangle-\varepsilon\langle\varphi_{x_1}^{(2)}\varphi_{x_2}^{(1)}|\varphi_{x_1}^{(1)}\varphi_{x_2}^{(2)}\rangle\right)\mathrm{d}^3x_1\mathrm{d}^3x_2=\\
=&\frac{1}{2}\left(\langle\varphi_{x_1}^{(1)}\varphi_{x_2}^{(2)}|\varphi_{x_1}^{(1)}\varphi_{x_2}^{(2)}\rangle+\langle\varphi_{x_1}^{(2)}\varphi_{x_2}^{(1)}|\varphi_{x_1}^{(2)}\varphi_{x_2}^{(1)}\rangle-\right.\\
&\left.-\varepsilon2\Re\left[\langle\varphi_{x_1}^{(1)}\varphi_{x_2}^{(2)}|\varphi_{x_1}^{(2)}\varphi_{x_2}^{(1)}\rangle\right]\right)\mathrm{d}^3x_1\mathrm{d}^3x_2.
\end{split}
\label{eq:69}
\end{align}
</mj>

上式中自旋$\|\chi\rangle$已经归一化，故不出现，$\varepsilon=\pm$分别对应自旋三重态和自旋单态；而

<mj>
\begin{equation}
\label{eq:70}
2\Re\left[\langle\varphi_{x_1}^{(1)}\varphi_{x_2}^{(2)}|\varphi_{x_1}^{(2)}\varphi_{x_2}^{(1)}\rangle\right]
\end{equation}
</mj>

被称为交换密度。

由式\eqref{eq:69}可知：  
1. 当两电子体系的自旋处于三重态$\|\chi^{(+)}\rangle$时，两电子出现在同一位置的概率趋于$0$，电子互相避开。这就是泡利排斥。
2. 当两电子体系的自旋处于单一态$\|\chi^{(-)}\rangle$时，两电子出现在同一位置的概率很大，电子互相吸引。这就是泡利吸引。

### 4.4 其他假定的应用及讨论
现在还要说明，在[4.1](#41-假定的陈述)中引入的对称化假定的范畴内，如何使用量子力学的基本假设，而不会产生矛盾。说的更加具体一点，就是如何利用只属于子空间$\mathcal{H}^{(+)}$或$\mathcal{H}^{(-)}$中的右矢去描述测量过程，并且证实与体系的态相关联的右矢$\|\psi(t)\rangle$在随时间的演变中不会越出这个子空间；也就是说，在子空间$\mathcal{H}^{(+)}$或$\mathcal{H}^{(-)}$内，整个量子理论体系都是适用的。

#### 4.4.1 有关测量的假定
现在考察对全同粒子体系进行的测量。根据对称化假定，描述体系在测量前的量子态的右矢$\|\psi(t)\rangle$，视体系由玻色子或费米子组成，属于子空间$\mathcal{H}^{(+)}$或$\mathcal{H}^{(-)}$。为了求体系处在给定物理状态的概率，应该用对应于体系在测量后的物理状态的右矢$\|u\rangle$去和$\|\psi(t)\rangle$构成标量积；右矢可以按照[4.3](#43-物理右矢的构成)中的法则构成，于是概率幅$\langle u\|\psi(t)\rangle$可以通过属于子空间$\mathcal{H}^{(+)}$或$\mathcal{H}^{(-)}$的两个矢量来表示。具体计算将在[4.4.3](#443-直接过程和间接过程之间的干涉)中讨论。

如果所要考察的测量是一个“完全的”测量（例如，确定全体粒子的位置和自旋分量），那么，物理右矢$\|u\rangle$是唯一的（只有常数因子的差异）；反之，如果测量不是“完全的”（例如，只测量自旋，或只对一个粒子进行测量），那么将得到若干个正交的物理右矢，这样，就应当求各对应概率的总和。

下面讨论，物理的观察算符对子空间$\mathcal{H}^{(+)}$或$\mathcal{H}^{(-)}$的作用。由于粒子的全同性，与所要考察的物理量相联系的观察算符对诸粒子而言都具有对称性。在$N$个全同粒子组成的体系中，实际可测的一切观察算符对$N$个粒子而言都具有对称性（见式\eqref{eq:12}），从而称这个对应的观察算符$\widehat{G}$为物理的观察算符。从数学上看，对$N$个粒子的一切交换而言，它应该是不变的；因此它应该和$N$粒子体系的所有置换算符$\mathcal{P}$对易（见式\eqref{eq:48}）：

<mj>
\begin{equation}
\label{eq:71}
[\widehat{G},\mathcal{P}]_-=0\quad\forall \mathcal{P}
\end{equation}
</mj>

例如，对易两个全同粒子的体系，观察算符$\hat{r}\_1-\hat{r}\_2$（两粒子位置矢量之差）在置换算符$P\_{12}$的作用下，并不是不变的（将变号），故这不是一个物理的观察算符；实际上，须能将粒子1和粒子2区分开才能对$\hat{r}\_1-\hat{r}\_2$进行测量。但我们可以测量两粒子之间的距离，即$\sqrt{(\hat{r}\_1-\hat{r}\_2)^2}$，这个量是对称的。

从式\eqref{eq:71}可见，在观察算符$\widehat{G}$的作用下，子空间$\mathcal{H}^{(+)}$和$\mathcal{H}^{(-)}$都是保持不变的。如果$\|\psi\rangle$属于子空间$\mathcal{H}^{(\varepsilon)}$，那么$\widehat{G}\|\psi\rangle$也属于$\mathcal{H}^{(\varepsilon)}$。实际上，右矢$\|\psi\rangle$属于子空间$\mathcal{H}^{(\varepsilon)}$意味着：

<mj>
\begin{equation}
\label{eq:72}
\mathcal{P}|\psi\rangle=\varepsilon|\psi\rangle
\end{equation}
</mj>

再来计算<mj>$\mathcal{P}\widehat{G}|\psi\rangle$</mj>，结合式\eqref{eq:71}，有：

<mj>
\begin{equation}
\label{eq:73}
\mathcal{P}\widehat{G}|\psi\rangle=\widehat{G}\mathcal{P}|\psi\rangle=\varepsilon\widehat{G}|\psi\rangle
\end{equation}
</mj>

上式表明$\widehat{G}$属于子空间$\mathcal{H}^{(\varepsilon)}$。

由此可见，通常可以施于一个观察算符的各种运算，特别是求本征值和本征矢的运算，在子空间$\mathcal{H}^{(\varepsilon)}$内，完全可以施于算符$\widehat{G}$，不过只保留算符$\widehat{G}$的那些属于物理子空间的本征右矢，已经相应本征值。

> **附注**：  
> 1. 如果局限于子空间$\mathcal{H}^{(\varepsilon)}$，那么算符$\widehat{G}$的存在于总空间$\mathcal{H}$的全体本征值就不一定都存在了。因此，对称化假定对一个对称的观察算符$\widehat{G}$的本征谱的影响就是（可能）取消某些本征值；另一方面，该假定不会给本征谱添加任何新的本征值，这是因为，在算符$\widehat{G}$的作用下，空间$\mathcal{H}^{(\varepsilon)}$具有整体不变性，因而算符$\widehat{G}$在子空间$\mathcal{H}^{(\varepsilon)}$中的全体本征矢也是其在空间$\mathcal{H}$的本征矢，并属于同样的本征值。  
> 2. 现在考虑数学上怎么用$\hat{r}\_1$，$\hat{p}\_1$，$\hat{s}\_1$等观察算符来表示前面列出的各类测量对应的观察算符，这个问题实际上并不简单。以三个全同粒子的体系为例，设法通过$\hat{r}\_1$，$\hat{r}\_2$和$\hat{r}\_3$来表示与三个位置同时测量相对应的观察算符。要解决这个问题，首先考虑若干个物理的观察算符，它们是如此选出的，即应能从这些观察算符中毫不含糊地得到各个粒子的位置（当然，不能给每个位置联系上一个已编号的粒子）；例如，可以选择这样的集合：
>
> <mj>\begin{equation}
\label{eq:74}
\hat{x}_1+\hat{x}_2+\hat{x}_3,\quad\hat{x}_1\hat{x}_2+\hat{x}_2\hat{x}_3+\hat{x}_3\hat{x}_1,\quad\hat{x}_1\hat{x}_2\hat{x}_3
\end{equation}</mj>
>
> （以及关于坐标$\hat{y}$和$\hat{z}$的诸对应观察算符）。但这里讨论的都是从纯形式的观点出发的；不要在一切情况下都试图写出观察算符的表达式，还是照前面的方法，只使用测量的物理本征右矢去做。

#### 4.4.2 有关时间演变的假定
一个全同粒子系的哈密顿算符一定是物理的观察算符。从式\eqref{eq:40}可见，所有置换算符都可以和体系的哈密顿算符对易：

\begin{equation}
\label{eq:75}
[\widehat{H},\mathcal{P}]\_-=0
\end{equation}

在这些条件下，如果描述体系在时刻$t\_0$初态的右矢$\|\psi(t\_0)\rangle$是一个物理右矢，那么由式\eqref{eq:54}可见所有置换算符与时间演化算符对易：

\begin{equation}
\label{eq:76}
[U,\mathcal{P}]\_-=0
\end{equation}

由此可见：

\begin{equation}
\label{eq:77}
\mathcal{P}|\psi(t)\rangle=\mathcal{P}U(t,t\_0)|\psi(t\_0)\rangle=U(t,t\_0)\mathcal{P}|\psi(t\_0)\rangle
\end{equation}

如果$\|\psi(t\_0)\rangle$是$\mathcal{P}$的本征矢，那么，$\|\psi(t)\rangle$也是它的本征矢，并属于同一个本征值。所以，右矢的完全对称化和完全反对称化的性质将一直保持不变。对称化假定与物理体系随时间演变的假定是相容的，即薛定谔方程不会使右矢$\|\psi\rangle$越出空间$\mathcal{H}^{(\varepsilon)}$。

#### 4.4.3 直接过程和间接过程之间的干涉
在量子力学中，关于一个体系的性质的所有预言都是通过概率幅（两个态矢量的标量积）或一个算符的矩阵元来表示的。可以想见，态矢量的对称化或反对称化可能会带来全同粒子系所特有的干涉效应。

考虑两个全同粒子的体系，已知其中一个处于单粒子态$\|\psi\_{\beta\_1}\rangle$，另一个处于单粒子态$\|\psi\_{\beta\_2}\rangle$。假设$\|\psi\_{\beta\_1}\rangle$和$\|\psi\_{\beta\_2}\rangle$是正交的，体系的态可以用下面的归一化右矢来描述（参见[4.3](#43-物理右矢的构成)）：

\begin{equation}
\label{eq:78}
\|\psi\_2^{(\varepsilon)}\rangle=\frac{1}{\sqrt{2}}(1+\varepsilon P\_{12})\|\psi\_{\beta\_1}^{(1)}\psi\_{\beta\_2}^{(2)}\rangle
\end{equation}

其中$\varepsilon=\pm$分别对应玻色子和费米子。

假设当粒子处于这个态时，我们想针对每一个粒子去测量同一个物理量$\widehat{\varphi}$，与此相联系的观察算符是$\widehat{\varphi}^{(1)}$和$\widehat{\varphi}^{(2)}$。为简单起见，假设$\widehat{\varphi}$的本征值是离散的且没有简并：

\begin{equation}
\label{eq:79}
\widehat{\varphi}\|\varphi\_{\alpha\_i}\rangle=\alpha\_i\|\varphi\_{\alpha\_i}\rangle
\end{equation}

现在要问，在这种测量中得到指定数据（对一个粒子是$\alpha\_1$，对另一个粒子是$\alpha\_2$）的概率是多大？先假设$\alpha\_1$和$\alpha\_2$不相等，则$\|\varphi\_{\alpha\_1}\rangle$和$\|\varphi\_{\alpha\_2}\rangle$是正交的。在此条件下，上述测量结果所确定的唯一归一化的物理右矢可以写作：

\begin{equation}
\label{eq:80}
\|\varphi\_2^{(\varepsilon)}\rangle=\frac{1}{\sqrt{2}}(1+\varepsilon P\_{12})\|\varphi\_{\alpha\_1}^{(1)}\varphi\_{\alpha\_2}^{(2)}\rangle
\end{equation}

由此可以得到与该测量结果相关联的概率幅：

\begin{equation}
\label{eq:81}
\langle\varphi\_2^{(\varepsilon)}\|\psi\_2^{(\varepsilon)}\rangle=\frac{1}{2}\langle\varphi\_{\alpha\_1}^{(1)}\varphi\_{\alpha\_2}^{(2)}\|(1+\varepsilon P\_{12}^\dagger)(1+\varepsilon P\_{12})\|\psi\_{\beta\_1}^{(1)}\psi\_{\beta\_2}^{(2)}\rangle
\end{equation}

利用位调算符的性质\eqref{eq:30}和\eqref{eq:34}可得：

\begin{equation}
\label{eq:82}
\frac{1}{2}(1+\varepsilon P\_{12}^\dagger)(1+\varepsilon P\_{12})=1+\varepsilon P\_{12}
\end{equation}

于是式\eqref{eq:81}变为：

\begin{equation}
\label{eq:83}
\langle\varphi\_2^{(\varepsilon)}\|\psi\_2^{(\varepsilon)}\rangle=\langle\varphi\_{\alpha\_1}^{(1)}\varphi\_{\alpha\_2}^{(2)}\|(1+\varepsilon P\_{12})\|\psi\_{\beta\_1}^{(1)}\psi\_{\beta\_2}^{(2)}\rangle
\end{equation}

将算符$1+\varepsilon P\_{12}$作用在左矢上得到：

<mj>
\begin{align}
\begin{split}
\langle\varphi_2^{(\varepsilon)}|\psi_2^{(\varepsilon)}\rangle=&\langle\varphi_{\alpha_1}^{(1)}\varphi_{\alpha_2}^{(2)}|\psi_{\beta_1}^{(1)}\psi_{\beta_2}^{(2)}\rangle+\varepsilon\langle\varphi_{\alpha_2}^{(1)}\varphi_{\alpha_1}^{(2)}|\psi_{\beta_1}^{(1)}\psi_{\beta_2}^{(2)}\rangle=\\
=&\langle\varphi_{\alpha_1}^{(1)}|\psi_{\beta_1}^{(1)}\rangle\langle\varphi_{\alpha_2}^{(2)}|\psi_{\beta_2}^{(2)}\rangle+\varepsilon\langle\varphi_{\alpha_2}^{(1)}|\psi_{\beta_1}^{(1)}\rangle\langle\varphi_{\alpha_1}^{(2)}|\psi_{\beta_2}^{(2)}\rangle=\\
=&\langle\varphi_{\alpha_1}|\psi_{\beta_1}\rangle\langle\varphi_{\alpha_2}|\psi_{\beta_2}\rangle+\varepsilon\langle\varphi_{\alpha_2}|\psi_{\beta_1}\rangle\langle\varphi_{\alpha_1}|\psi_{\beta_2}\rangle
\end{split}
\label{eq:84}
\end{align}
</mj>

这样一来，诸粒子的编号便消失了，概率幅可以通过诸标量积的函数$\langle\varphi\_{\alpha\_1}\|\psi\_{\beta\_1}\rangle\cdots\langle\varphi\_{\alpha\_1}\|\psi\_{\beta\_2}\rangle$来表示。概率幅成为两项之和（对于玻色子）或两项之差（对于费米子）。

\eqref{eq:84}式中结果的解释如下：可以通过两种不同的“途径”将对应于初态的两个右矢$\|\psi\_{\beta\_1}\rangle$和$\|\psi\_{\beta\_2}\rangle$联系上对应于末态的两个左矢$\langle\varphi\_{\alpha\_1}\|$和$\langle\varphi\_{\alpha\_2}\|$；这两种途径中的每一种都对应着一个概率幅，即$\langle\varphi\_{\alpha\_1}\|\psi\_{\beta\_1}\rangle\langle\varphi\_{\alpha\_2}\|\psi\_{\beta\_2}\rangle$或$\langle\varphi\_{\alpha\_2}\|\psi\_{\beta\_1}\rangle\langle\varphi\_{\alpha\_1}\|\psi\_{\beta\_2}\rangle$，而这两种概率幅，在玻色子的情况下以$+$号相干涉；在费米子的情况下以$-$号相干涉。现在就得到在[2.3](#23-量子力学中的全同粒子)中所提问题的答案：待求的概率$\mathcal{p}(\alpha\_1;\alpha\_2)$应等于式\eqref{eq:84}的模的平方：

\begin{equation}
\label{eq:85}
\mathcal{p}(\alpha\_1;\alpha\_2)=\|\langle\varphi\_{\alpha\_1}\|\psi\_{\beta\_1}\rangle\langle\varphi\_{\alpha\_2}\|\psi\_{\beta\_2}\rangle+\varepsilon\langle\varphi\_{\alpha\_2}\|\psi\_{\beta\_1}\rangle\langle\varphi\_{\alpha\_1}\|\psi\_{\beta\_2}\rangle\|^2
\end{equation}

通常，将式\eqref{eq:84}中最后一个等式中第一项那样的项叫做直接项，另一项（含有$\varepsilon$）叫做交换项。

> **附注**：  
> 现在来讨论一下，若两个粒子并非全同时情况会怎么样。作为体系的初态，取张量积右矢：
>
> \begin{equation}
\label{eq:86}
\|\psi\rangle=\|\psi\_{\beta\_1}^{(1)}\psi\_{\beta\_2}^{(2)}\rangle
\end{equation}
>
> 再设想一种测量仪器，尽管粒子1和粒子2并非全同，但它不能区别；如果仪器给出的结果是$\alpha\_1$和$\alpha\_2$，也无法得知$\alpha\_1$是与粒子1相关还是与粒子2相关（例如，体系含有一个$\mu^-$子和一个电子$e^-$，而仪器只对粒子的电荷有影响，对于质量却不能提供任何信息）。于是两个本征态$\|\varphi\_{\alpha\_1}^{(1)}\varphi\_{\alpha\_2}^{(2)}\rangle$和$\|\varphi\_{\alpha\_2}^{(1)}\varphi\_{\alpha\_1}^{(2)}\rangle$（在此情况下，两者表示不同的物理状态）对应着同一个测量结果；因为两者是正交的，应将相应的概率相加，便得到：
>
> <mj>\begin{align}
\begin{split}
\mathcal{p}'(\alpha_1;\alpha_2)=&|\langle\varphi_{\alpha_1}^{(1)}\varphi_{\alpha_2}^{(2)}|\psi_{\beta_1}^{(1)}\psi_{\beta_2}^{(2)}\rangle|^2+|\langle\varphi_{\alpha_2}^{(1)}\varphi_{\alpha_1}^{(2)}|\psi_{\beta_1}^{(1)}\psi_{\beta_2}^{(2)}\rangle|^2=\\
=&|\langle\varphi_{\alpha_1}|\psi_{\beta_1}\rangle|^2|\langle\varphi_{\alpha_2}|\psi_{\beta_2}\rangle|^2+|\langle\varphi_{\alpha_2}|\psi_{\beta_1}\rangle|^2|\langle\varphi_{\alpha_1}|\psi_{\beta_2}\rangle|^2
\end{split}
\label{eq:87}
\end{align}</mj>
>
> 比较\eqref{eq:85}和\eqref{eq:87}便可以清楚地看到，量子力学的预言，视粒子为全同的或非全同的，而存在重大差别。

下面考虑两个态$\|\varphi\_{\alpha\_1}\rangle$和$\|\varphi\_{\alpha\_2}\rangle$相同的情况。如果两个粒子是费米子，根据泡利不相容原理，概率$\mathcal{p}(\alpha\_1;\alpha\_1)$等于零。反之如果两个粒子是玻色子，便有：

\begin{equation}
\label{eq:88}
\|\varphi\_2^{(+)}\rangle=\|\varphi\_{\alpha\_1}^{(1)}\varphi\_{\alpha\_1}^{(2)}\rangle
\end{equation}

从而

<mj>
\begin{align}
\label{eq:89}
\begin{split}
\langle\varphi_2^{(+)}|\psi_2^{(+)}\rangle&=\frac{1}{\sqrt{2}}\langle\varphi_{\alpha_1}^{(1)}\varphi_{\alpha_1}^{(2)}|(1+P_{12})|\psi_{\beta_1}^{(1)}\psi_{\beta_2}^{(2)}\rangle=\\\
&=\sqrt{2}\langle\varphi_{\alpha_1}|\psi_{\beta_1}\rangle\langle\varphi_{\alpha_1}|\psi_{\beta_2}\rangle
\end{split}
\end{align}
</mj>

由此得到：

<mj>
\begin{equation}
\label{eq:90}
\mathcal{p}(\alpha_1;\alpha_1)=2|\langle\varphi_{\alpha_1}|\psi_{\beta_1}\rangle\langle\varphi_{\alpha_1}|\psi_{\beta_2}\rangle|^2
\end{equation}
</mj>

> **附注**：  
> 前面讨论过两者并非全同粒子的情况，现在将这种情况下可能得到的结果与上面的结果比较一下。此时应以$\|\psi\_{\beta\_1}^{(1)}\psi\_{\beta\_2}^{(2)}\rangle$代替$\|\psi\_2^{(\varepsilon)}\rangle$，用$\|\varphi\_{\alpha\_1}^{(1)}\varphi\_{\alpha\_1}^{(2)}\rangle$代替$\|\varphi\_2^{(\varepsilon)}\rangle$然后得到概率幅
>
> \begin{equation}
\label{eq:91}
\langle\varphi\_{\alpha\_1}\|\psi\_{\beta\_1}\rangle\langle\varphi\_{\alpha\_1}\|\psi\_{\beta\_2}\rangle
\end{equation}
>
> 从而
>
> \begin{equation}
\label{eq:92}
\mathcal{p}'(\alpha\_1;\alpha\_1)=\|\langle\varphi\_{\alpha\_1}\|\psi\_{\beta\_1}\rangle\langle\varphi\_{\alpha\_1}\|\psi\_{\beta\_2}\rangle\|^2
\end{equation}
>
> 对于含有$N$个全同粒子的体系，一般来说有$N!$个不同的交换项，它们在概率幅中相加（相减）。

下面以两个全同粒子的弹性碰撞为例，详细说明交换项的物理意义（在[2.3](#23-量子力学中的全同粒子)已经提及）。与之前的做法不同，现在需要考虑体系从初始时刻$t\_0$的态$\|\psi(t\_0)\rangle$到测量时刻$t$的态$\|\psi(t)\rangle$之间的演变。下面将看到，这种演变不会使问题在根本上有所改变，交换项仍以前面的方式出现。

在体系的初态中，两个粒子以相反的动量相向而行。设一个粒子初始动量为$\mathbf{p}$，则另一个为$-\mathbf{p}$。将表示这个初态的物理右矢写成下列形式：

\begin{equation}
\label{eq:93}
\|\psi(t\_0)\rangle=\frac{1}{\sqrt{2}}(1+\varepsilon P\_{12})\|\psi\_{\mathbf{p}}^{(1)}\psi\_{-\mathbf{p}}^{(2)}\rangle
\end{equation}

支配体系随时间演变的薛定谔方程是线性的，存在时间演化算符$U$，它是哈密顿算符$\widehat{H}$的函数，使得$t$时刻的态矢量可以表示为：

\begin{equation}
\label{eq:94}
\|\psi(t)\rangle=U(t,t\_0)\|\psi(t\_0)\rangle
\end{equation}

现在来计算在在[2.3](#23-量子力学中的全同粒子)提及的测量结果的概率幅，在那里探测器D所在方向两个粒子的动量为$\mathbf{p}'$和$-\mathbf{p}'$，动量$\mathbf{p}'$与$\mathbf{p}$大小相等，将对应这个末态的物理右矢记作：

\begin{equation}
\label{eq:95}
\|\psi\_D\rangle=\frac{1}{\sqrt{2}}(1+\varepsilon P\_{12})\|\psi\_{\mathbf{p}'}^{(1)}\psi\_{-\mathbf{p}'}^{(2)}\rangle
\end{equation}

于是所求的概率幅可以写作：

<mj>
\begin{align}
\begin{split}
\langle\psi_D|\psi(t)\rangle=&\langle\psi_D|U(t,t_0)\psi(t)\rangle=\\
=&\frac{1}{2}\langle\psi_{\mathbf{p}'}^{(1)}\psi_{-\mathbf{p}'}^{(2)}|(1+\varepsilon P_{12}^\dagger)U(t,t_0)(1+\varepsilon P_{12})|\psi_{\mathbf{p}}^{(1)}\psi_{-\mathbf{p}}^{(2)}\rangle=\\
=&\langle\psi_{\mathbf{p}'}^{(1)}\psi_{-\mathbf{p}'}^{(2)}|(1+\varepsilon P_{12}^\dagger)U(t,t_0)|\psi_{\mathbf{p}}^{(1)}\psi_{-\mathbf{p}}^{(2)}\rangle=\\
=&\langle\psi_{\mathbf{p}'}^{(1)}\psi_{-\mathbf{p}'}^{(2)}|U(t,t_0)|\psi_{\mathbf{p}}^{(1)}\psi_{-\mathbf{p}}^{(2)}\rangle+\\
&+\varepsilon\langle\psi_{-\mathbf{p}'}^{(1)}\psi_{\mathbf{p}'}^{(2)}|U(t,t_0)|\psi_{\mathbf{p}}^{(1)}\psi_{-\mathbf{p}}^{(2)}\rangle
\end{split}
\label{eq:96}
\end{align}
</mj>

上式第三行利用了式\eqref{eq:76}和式\eqref{eq:82}。由此可见，直接项相当于[2.3](#23-量子力学中的全同粒子)中的a道路，间接项就对应于b道路。在此例中，仍然应该将相应的概率幅相加（玻色子）或相减（费米子），这样一来，如果取式\eqref{eq:96}的模平方，就会出现一个干涉项。还须注意，如果将$\mathbf{p}$换作$-\mathbf{p}$，这个式子不过多了一个乘数$\varepsilon$，对应的概率并不会改变。

#### 4.4.4 可以忽略对称化假定的一些情况
如果处处都必须应用对称化假定，那么，当体系中的粒子数受到限制时，将无法研究此体系的性质，因为必须考虑到宇宙中与此粒子全同的所有粒子。实际情况并非如此，在某些特殊情况下，全同粒子在性质上类似于性质不同的粒子，为了得到正确的物理预言，没有必要引用对称化假定。注意到[4.4.3](#443-直接过程和间接过程之间的干涉)中的结果，很自然地想到，每当对称化假定引入的交换项等于零时，就会出现这种情况。下面举两个例子来说明这种情况。

首先考虑处于空间的两个不同区域中的全同粒子，这两个粒子一个处于单粒子态$\|\varphi\rangle$，另一个处于单粒子态$\|\chi\rangle$，这里不考虑自旋。假设表示右矢$\|\varphi\rangle$和$\|\chi\rangle$的波函数的定义域在空间是分开的：

<mj>
\begin{equation}
\label{eq:97}
\begin{cases}
\varphi(\mathbf{r})=\langle\mathbf{r}|\varphi\rangle=0,\quad\text{if}\quad\mathbf{r}\notin D\\
\chi(\mathbf{r})=\langle\mathbf{r}|\chi\rangle=0,\quad\text{if}\quad\mathbf{r}\notin\Delta
\end{cases}
\end{equation}
</mj>

这里区域$D$和$\Delta$是分开的。此时便相当于经典力学中的情况（[2.2](#22-经典力学中的全同粒子)）：只要区域$D$和$\Delta$并不重叠，就可以“跟踪”每一个粒子；于是可以预见，对称化假定在此并无必要。现在设想使用两套不同的仪器对两个粒子同时进行测量，一套仪器对发生在区域$\Delta$中的现象没有响应，另一套对区域$D$中的没有响应。假设与两套仪器测量结果相关联的单粒子态分别为$\|u\rangle$和$\|v\rangle$。既然粒子是全同的，原则上应引用对称化假定。于是，在与测量结果相关的概率幅中，直接项就是$\langle u\|\varphi\rangle\langle v\|\chi\rangle$，交换项就是$\langle u\|\chi\rangle\langle v\|\varphi\rangle$。但测量仪器在空间的安排意味着：

<mj>
\begin{equation}
\label{eq:98}
\begin{cases}
u(\mathbf{r})=\langle\mathbf{r}|u\rangle=0,\quad\text{if}\quad\mathbf{r}\in\Delta\\
v(\mathbf{r})=\langle\mathbf{r}|v\rangle=0,\quad\text{if}\quad\mathbf{r}\in D
\end{cases}
\end{equation}
</mj>

由\eqref{eq:97}和\eqref{eq:98}可以得到：

\begin{equation}
\label{eq:99}
\langle u\|\chi\rangle=\langle v\|\varphi\rangle=0
\end{equation}

由此可见，交换项为零，没有必要引入对称化假定。实际上，可将两者看成性质互异的粒子，给区域$D$中的粒子编号为1，给区域$\Delta$中粒子编号为2；如此进行分析：测量前，体系的态由右矢$\|\varphi^{(1)}\chi^{(2)}\rangle$描述，与测量结果相关的右矢为$\|u^{(1)}v^{(2)}\rangle$，两者标量积就是概率幅$\langle u\|\varphi\rangle\langle v\|\chi\rangle$。

上述分析表明，全同粒子的存在并不妨碍孤立地研究含有少数粒子受约束的体系。

> **附注**：  
> 上述体系不仅要在初态处于两个不同的区域中，在演变之后依然要限制于两个不同的区域中，且两者间不能有相互作用。实际上，不论粒子是否全同，相互作用总是在两者间引入了相关性，于是，不再可能用单粒子态矢量去描述两个粒子中的每一个。

再来考虑可以按自旋取向来鉴别的粒子，考察两个自旋为$1/2$的全同粒子（譬如电子）之间的弹性碰撞，假设自旋的相互作用可忽略，且两粒子自旋态在碰撞过程中保持不变。如果这两个自旋态最初是正交的，那么，根据自旋态就可以在任何时刻区分这两个粒子，如同根据互异粒子的固有属性将其区分，此时对称化假定失去效用。

具体来说，[4.4.3](#443-直接过程和间接过程之间的干涉)中的碰撞例子中，每个动量指标后面都要加上一个确定的自旋分量指标（$+$号或$-$号），这样一来式\eqref{eq:96}最后一个等式中只有第一项不为零，第二项可以写作：

\begin{equation}
\label{eq:100}
\langle\psi\_{-\mathbf{p}',-}^{(1)}\psi\_{\mathbf{p}',+}^{(2)}\|U(t,t\_0)\|\psi\_{\mathbf{p},+}^{(1)}\psi\_{-\mathbf{p},-}^{(2)}\rangle
\end{equation}

这是一个（据假设）与自旋无关的算符在两右矢之间的矩阵元，而两右矢中的自旋是正交的，于是其结果为零。因此，可以将这两个粒子当作非全同粒子处理，并根据自旋将其编号，也能得到同样的结果。当然，如果演化算符$U$，或者更直接地说，体系的哈密顿算符$\widehat{H}$，依赖于自旋，上述方法便不适用。

## 5 形式化的二次量子化
二次量子化的形式大大简化了多粒子系统的描述，但归根结底，也仅仅是对原始的薛定谔方程做了形式上的重构，对方程的解并没有做出新的贡献。二次量子化的重要特征是产生湮灭算符，这样一来就免去了书写冗长的对称化或反对称化右矢的麻烦，所有的统计特征都能包含在产生湮灭算符间的基本对易关系里，多体系统间的相互作用也可以表述为粒子的产生和湮灭。基于前面的结论，现在分别给出连续本征谱和离散本征谱情况下的二次量子化形式。

### 5.1 “连续的”福克表象
为了使引入产生湮灭算符的过程简单而顺利，不妨做一些预先的设定。首先定义有连续本征谱的单粒子观察算符$\widehat{\varphi}$：

<mj>
\begin{align}
\widehat{\varphi}|\varphi_\alpha\rangle&=\varphi_\alpha|\varphi_\alpha\rangle\label{eq:101}\\
\langle\varphi_\alpha|\varphi_\beta\rangle&=\delta(\varphi_\alpha-\varphi_\beta)\equiv\delta(\alpha-\beta)\label{eq:102}
\end{align}
</mj>

这些本征态构成$\mathcal{H}\_1$的一组基：

\begin{equation}
\label{eq:103}
\int\mathrm{d}\varphi\_\alpha\|\varphi\_\alpha\rangle\langle\varphi\_\alpha\|=\mathbf{1}
\end{equation}

一个没有对称化的$N$粒子态（类似于式\eqref{eq:4}）是简单的单粒子态的直积：

\begin{equation}
\label{eq:104}
\|\varphi\_{\alpha\_1}\varphi\_{\alpha\_2}\cdots\varphi\_{\alpha\_N}\rangle=\|\varphi\_{\alpha\_1}^{(1)}\rangle\|\varphi\_{\alpha\_2}^{(2)}\rangle\cdots\|\varphi\_{\alpha\_N}^{(N)}\rangle
\end{equation}

上标$(i)$代表粒子，下标$\alpha\_i$是量子数的完全集。$N$重态指标$\alpha\_i$任意排序，但遵循某个定义好的准则，上式左边项（没有粒子指标）意味着这是一个标准排序。利用式\eqref{eq:56}中的$\widehat{S}\_\varepsilon$将式\eqref{eq:104}转化为一个对称化（反对称化）的$N$粒子态：

\begin{equation}
\label{eq:105}
\|\varphi\_{\alpha\_1}\varphi\_{\alpha\_2}\cdots\varphi\_{\alpha\_N}\rangle^{(\varepsilon)}=\frac{1}{N!}\sum\_\mathcal{P}\varepsilon^p\mathcal{P}\|\varphi\_{\alpha\_1}\varphi\_{\alpha\_2}\cdots\varphi\_{\alpha\_N}\rangle
\end{equation}

这里引入归一化因子$1/N!$（可参考对称群）。在不至于引起混淆的情况下将态\eqref{eq:105}简记为$\|\varphi\_N^{(\varepsilon)}\rangle$。

在态空间$\mathcal{H}\_N^{(\varepsilon)}$中，每个置换算符$\mathcal{P}$都是厄密的：

<mj>
\begin{align}
\label{eq:106}
\begin{split}
\langle\varphi_N^{(\varepsilon)}|\mathcal{P}^\dagger|\varphi_N^{(\varepsilon)}\rangle&=\left(\langle\varphi_N^{(\varepsilon)}|\mathcal{P}|\varphi_N^{(\varepsilon)}\rangle\right)^*=\varepsilon^p\left(\langle\varphi_N^{(\varepsilon)}|\varphi_N^{(\varepsilon)}\rangle\right)^*=\\
&=\varepsilon^p\langle\varphi_N^{(\varepsilon)}|\varphi_N^{(\varepsilon)}\rangle=\langle\varphi_N^{(\varepsilon)}|\mathcal{P}|\varphi_N^{(\varepsilon)}\rangle
\end{split}
\end{align}
</mj>

由此得到：

\begin{equation}
\label{eq:107}
\mathcal{P}=\mathcal{P}^\dagger\quad\text{within}\quad\mathcal{H}\_N^{(\varepsilon)}
\end{equation}

从式\eqref{eq:105}还可以得到这样一个有用的关系，对任意一个观察算符$\widehat{A}$总有如下关系：

<mj>
\begin{align}
\label{eq:108}
\begin{split}
\langle\psi_N^{(\varepsilon)}|\widehat{A}|\varphi_N^{(\varepsilon)}\rangle&=\frac{1}{N!}\sum_\mathcal{P}\varepsilon^p\langle\psi_{\alpha_1}\psi_{\alpha_2}\cdots\psi_{\alpha_N}|\mathcal{P}^\dagger\widehat{A}|\varphi_N^{(\varepsilon)}\rangle=\\\
&=\frac{1}{N!}\sum_\mathcal{P}\varepsilon^p\langle\psi_{\alpha_1}\psi_{\alpha_2}\cdots\psi_{\alpha_N}|\widehat{A}\mathcal{P}|\varphi_N^{(\varepsilon)}\rangle=\\\
&=\frac{1}{N!}\sum_\mathcal{P}\varepsilon^{2p}\langle\psi_{\alpha_1}\psi_{\alpha_2}\cdots\psi_{\alpha_N}|\widehat{A}|\varphi_N^{(\varepsilon)}\rangle
\end{split}
\end{align}
</mj>

上式的第二行利用了式\eqref{eq:71}和式\eqref{eq:107}。由于$\varepsilon^{2p}=1$，上式对$N!$个相同的项求和就得到：

\begin{equation}
\label{eq:109}
\langle\psi\_N^{(\varepsilon)}\|\widehat{A}\|\varphi\_N^{(\varepsilon)}\rangle=\langle\psi\_{\alpha\_1}\psi\_{\alpha\_2}\cdots\psi\_{\alpha\_N}\|\widehat{A}\|\varphi\_N^{(\varepsilon)}\rangle
\end{equation}

上式右端的左矢并没有对称化。特别地，当$\widehat{A}$是单位算符时：

<mj>
\begin{align}
\label{eq:110}
\begin{split}
&{}^{(\varepsilon)}\langle\varphi_{\beta_1}\cdots\varphi_{\beta_N}|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}=\\
&=\langle\varphi_{\beta_1}\cdots\varphi_{\beta_N}|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}=\\
&=\frac{1}{N!}\sum_{\mathcal{P}_\alpha}\varepsilon^{p_\alpha}\mathcal{P}_\alpha\langle\varphi_{\beta_1}\cdots\varphi_{\beta_N}|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle
\end{split}
\end{align}
</mj>

下标$\alpha$表示$\mathcal{P}\_\alpha$只是作用在$\varphi\_\alpha$上。于是便得到两个对称化（反对称化）的$N$粒子态的标量积：

<mj>
\begin{align}
\begin{split}
&{}^{(\varepsilon)}\langle\varphi_{\beta_1}\cdots\varphi_{\beta_N}|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}=\\
&=\frac{1}{N!}\sum_{\mathcal{P}_\alpha}\varepsilon^{p_\alpha}\mathcal{P}_\alpha\left\{\langle\varphi_{\beta_1}^{(1)}|\varphi_{\alpha_1}^{(1)}\rangle\cdots\langle\varphi_{\beta_N}^{(N)}|\varphi_{\alpha_N}^{(N)}\rangle\right\}=\\
&=\frac{1}{N!}\sum_{\mathcal{P}_\alpha}\varepsilon^{p_\alpha}\mathcal{P}_\alpha\left[\delta(\beta_1-\alpha_1)\cdots\delta(\beta_N-\alpha_N)\right].
\end{split}
\label{eq:111}
\end{align}
</mj>

从逻辑上看，上式是对单粒子态正交性\eqref{eq:102}的推广，从上式可以得到：

<mj>
\begin{align}
\begin{split}
&\int\cdots\int\mathrm{d}\beta_1\cdots\mathrm{d}\beta_N|\varphi_{\beta_1}\cdots\varphi_{\beta_N}\rangle^{(\varepsilon)}{}^{(\varepsilon)}\langle\varphi_{\beta_1}\cdots\varphi_{\beta_N}|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}=\\
&=\frac{1}{N!}\sum_{\mathcal{P}_\alpha}\varepsilon^{p_\alpha}\mathcal{P}_\alpha|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}=\frac{1}{N!}\sum_{\mathcal{P}_\alpha}\varepsilon^{2p_\alpha}|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}=\\
&=|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}
\end{split}
\label{eq:112}
\end{align}
</mj>

任意一个$N$粒子态$\|\psi\_N\rangle^{(\varepsilon)}$都可以表示成$N$个单粒子态$\|\psi\rangle$的直积之和。既然假定$\|\varphi\_\alpha\rangle$构成$\mathcal{H}\_1$的完备基，$\|\psi\rangle$可由$\|\varphi\_\alpha\rangle$线性表出，那么$\|\psi\_N\rangle^{(\varepsilon)}$自然可以由$\|\varphi\_{\alpha\_1}\cdots\rangle^{(\varepsilon)}$线性表出：

<mj>
\begin{align}
\label{eq:113}
\begin{split}
|\psi_N\rangle^{(\varepsilon)}&=\widehat{S}_\varepsilon|\psi^{(1)}\cdots\psi^{(N)}\rangle=\\
&=\sum_{\alpha_1}C_{\alpha_1}\sum_{\alpha_2}C_{\alpha_2}\cdots\sum_{\alpha_N}C_{\alpha_N}\widehat{S}_\varepsilon|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle=\\
&=\sum_{\alpha_1\cdots\alpha_N}C(\alpha_1\cdots\alpha_N)|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}
\end{split}
\end{align}
</mj>

从式\eqref{eq:112}可得完全性关系：

\begin{equation}
\label{eq:114}
\int\cdots\int\mathrm{d}\beta\_1\cdots\mathrm{d}\beta\_N\|\varphi\_{\beta\_1}\cdots\varphi\_{\beta\_N}\rangle^{(\varepsilon)}{}^{(\varepsilon)}\langle\varphi\_{\beta\_1}\cdots\varphi\_{\beta\_N}\|=\mathbf{1}\quad\text{within}\quad\mathcal{H}\_N^{(\varepsilon)}
\end{equation}

由此可见式\eqref{eq:105}所定义的态$\|\varphi\_{\alpha\_1}\cdots\varphi\_{\alpha\_N}\rangle^{(\varepsilon)}$构成$\mathcal{H}\_N^{(\varepsilon)}$的一组正交完备基。

前面这么多的铺垫恰恰证明用对称化（反对称化）的$N$粒子态来讨论问题是多么冗杂无趣。好在通过一种特殊的算符，这些长长的（形式上）态完全可以从所谓的真空态构造出来：

\begin{equation}
\label{eq:115}
\text{vaccum state }\|0\rangle;\quad\langle0\|0\rangle=1
\end{equation}

这个算符：

\begin{equation}
\label{eq:116}
a\_{\varphi\_\alpha}^\dagger\equiv a\_\alpha^\dagger
\end{equation}

的特性就是将不同粒子数的希尔伯特空间相互联系：

\begin{equation}
\label{eq:117}
a\_\alpha^\dagger:\mathcal{H}\_N^{(\varepsilon)}\Longrightarrow\mathcal{H}\_{N+1}^{(\varepsilon)}
\end{equation}

这个算符完全由它的效果定义：

<mj>
\begin{equation}
\label{eq:118}
\begin{array}{c}
a_{\alpha_1}^\dagger|0\rangle=\sqrt{1}|\varphi_{\alpha_1}\rangle^{(\varepsilon)},\\
a_{\alpha_2}^\dagger|\varphi_{\alpha_1}\rangle^{(\varepsilon)}=\sqrt{2}|\varphi_{\alpha_2}\varphi_{\alpha_1}\rangle^{(\varepsilon)}\\
\cdots
\end{array}
\end{equation}
</mj>

写成一般形式：

\begin{equation}
\label{eq:119}
a\_\beta^\dagger\underbrace{\|\varphi\_{\alpha\_1}\cdots\varphi\_{\alpha\_N}\rangle^{(\varepsilon)}}\_{\in\mathcal{H}\_N^{(\varepsilon)}}=\sqrt{N+1}\underbrace{\|\varphi\_\beta\varphi\_{\alpha\_1}\cdots\varphi\_{\alpha\_N}\rangle^{(\varepsilon)}}\_{\in\mathcal{H}\_{N+1}^{(\varepsilon)}}
\end{equation}

这个$a\_\beta^\dagger$就是所谓的产生算符，对应的物理图像就是产生一个处于单粒子态$\|\varphi\_\beta\rangle$的新粒子。把式\eqref{eq:119}倒过来看就是：

\begin{equation}
\label{eq:120}
\|\varphi\_{\alpha\_1}\cdots\varphi\_{\alpha\_N}\rangle^{(\varepsilon)}=\frac{1}{\sqrt{N!}}a\_{\alpha\_1}^\dagger a\_{\alpha\_2}^\dagger\cdots a\_{\alpha\_N}^\dagger\|0\rangle
\end{equation}

处理算符的操作顺序时须谨慎，例如

\begin{equation}
\label{eq:121}
a\_{\alpha\_1}^\dagger a\_{\alpha\_2}^\dagger\|\varphi\_{\alpha\_3}\cdots\varphi\_{\alpha\_N}\rangle^{(\varepsilon)}=\sqrt{N(N-1)}\|\varphi\_{\alpha\_1}\varphi\_{\alpha\_2}\varphi\_{\alpha\_3}\cdots\varphi\_{\alpha\_N}\rangle^{(\varepsilon)}
\end{equation}

而
<mj>
\begin{align}
\label{eq:122}
\begin{split}
a_{\alpha_2}^\dagger a_{\alpha_1}^\dagger|\varphi_{\alpha_3}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}&=\sqrt{N(N-1)}|\varphi_{\alpha_2}\varphi_{\alpha_1}\varphi_{\alpha_3}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}=\\
&=\varepsilon\sqrt{N(N-1)}|\varphi_{\alpha_1}\varphi_{\alpha_2}\varphi_{\alpha_3}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}
\end{split}
\end{align}
</mj>

基于上面两式可得如下算符恒等式：

\begin{equation}
\label{eq:123}
[a\_{\alpha\_1}^\dagger,a\_{\alpha\_2}^\dagger]\_{-\varepsilon}=a\_{\alpha\_1}^\dagger a\_{\alpha\_2}^\dagger-\varepsilon a\_{\alpha\_2}^\dagger a\_{\alpha\_1}^\dagger=0
\end{equation}

产生算符的对于玻色子是对易的（$\varepsilon=+$），对于费米子是反对易的（$\varepsilon=-$）。

现在讨论$a\_\alpha^\dagger$的共轭算符，

\begin{equation}
\label{eq:124}
a\_\alpha=\left(a\_\alpha^\dagger\right)^\dagger
\end{equation}

它将$\mathcal{H}\_N^{(\varepsilon)}$和$\mathcal{H}\_{N-1}^{(\varepsilon)}$相互连接：

\begin{equation}
\label{eq:125}
a\_\alpha:\mathcal{H}\_N^{(\varepsilon)}\Longrightarrow\mathcal{H}\_{N-1}^{(\varepsilon)}
\end{equation}

这就是所谓的湮灭算符，既然它是$a\_\alpha^\dagger$的共轭，从\eqref{eq:119}和\eqref{eq:120}可见：

<mj>
\begin{align}
{}^{(\varepsilon)}\langle\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}|a_\beta&=\sqrt{N+1}{}^{(\varepsilon)}\langle\varphi_\beta\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}|\label{eq:126}\\
{}^{(\varepsilon)}\langle\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}|&=\frac{1}{\sqrt{N!}}\langle0|a_{\alpha_N}\cdots a_{\alpha_2}a_{\alpha_1}\label{eq:127}\\
\end{align}
</mj>

$a\_\alpha$的物理意义可以通过计算以下矩阵元进一步明晰：

<mj>
\begin{align}
\label{eq:128}
\begin{split}
&{}^{(\varepsilon)}\left\langle\underbrace{\varphi_{\beta_2}\cdots\varphi_{\beta_N}}_{\in\mathcal{H}_{N-1}^{(\varepsilon)}}|a_\gamma|\underbrace{\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}}_{\in\mathcal{H}_N^{(\varepsilon)}}\right\rangle^{(\varepsilon)}=\\
&=\sqrt{N}{}^{(\varepsilon)}\langle\varphi_\gamma\varphi_{\beta_2}\cdots\varphi_{\beta_N}|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}=\\
&=\frac{\sqrt{N}}{N!}\sum_{\mathcal{P}_\alpha}\varepsilon^{p_\alpha}\mathcal{P}_\alpha\left(\delta(\gamma-\alpha_1)\delta(\beta_2-\alpha_2)\cdots\delta(\beta_N-\alpha_N)\right)
\end{split}
\end{align}
</mj>

上式的最后一步用了式\eqref{eq:111}。将求和项重排（以$\delta(\gamma-\alpha\_i)$分成$N$个小的求和）：

<mj>
\begin{align}
\label{eq:129}
\begin{split}
&{}^{(\varepsilon)}\langle\varphi_{\beta_2}\cdots\varphi_{\beta_N}|a_\gamma|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}=\\
=&\frac{1}{\sqrt{N}}\frac{1}{(N-1)!}\left\{\delta(\gamma-\alpha_1)\sum_{\mathcal{P}_\alpha}\varepsilon^{p_\alpha}\mathcal{P}_\alpha\left(\delta(\beta_2-\alpha_2)\cdots\delta(\beta_N-\alpha_N)\right)+\right.\\
&+\varepsilon\delta(\gamma-\alpha_2)\sum_{\mathcal{P}_\alpha}\varepsilon^{p_\alpha}\mathcal{P}_\alpha\left(\delta(\beta_2-\alpha_1)\delta(\beta_3-\alpha_3)\cdots\delta(\beta_N-\alpha_N)\right)+\\\
&+\cdots+\\\
&\left.+\varepsilon^{N-1}\delta(\gamma-\alpha_N)\sum_{\mathcal{P}_\alpha}\varepsilon^{p_\alpha}\mathcal{P}_\alpha\left(\delta(\beta_2-\alpha_1)\delta(\beta_3-\alpha_2)\cdots\delta(\beta_N-\alpha_{N-1})\right)\right\}
\end{split}
\end{align}
</mj>

上式右边的每个小的求和项也表示标量积，只不过是$\mathcal{H}\_{N-1}^{(\varepsilon)}$内的，将$1/(N-1)!$拿进去，再次利用\eqref{eq:111}：

<mj>
\begin{align}
\label{eq:130}
\begin{split}
&{}^{(\varepsilon)}\langle\varphi_{\beta_2}\cdots\varphi_{\beta_N}|a_\gamma|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}=\\
=&\frac{1}{\sqrt{N}}\left\{\delta(\gamma-\alpha_1){}^{(\varepsilon)}\langle\varphi_{\beta_2}\cdots\varphi_{\beta_N}|\varphi_{\alpha_2}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}+\right.\\
&+\varepsilon\delta(\gamma-\alpha_2){}^{(\varepsilon)}\langle\varphi_{\beta_2}\cdots\varphi_{\beta_N}|\varphi_{\alpha_1}\varphi_{\alpha_3}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}+\\
&+\cdots+\\\
&\left.+\varepsilon^{N-1}\delta(\gamma-\alpha_N){}^{(\varepsilon)}\langle\varphi_{\beta_2}\cdots\varphi_{\beta_N}|\varphi_{\alpha_1}\cdots\varphi_{\alpha_{N-1}}\rangle^{(\varepsilon)}\right\}
\end{split}
\end{align}
</mj>

由于左矢是$\mathcal{H}\_{N-1}^{(\varepsilon)}$内的任意基矢，上式表明：

<mj>
\begin{align}
\begin{split}
a_\gamma|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}=&\frac{1}{\sqrt{N}}\left\{\delta(\gamma-\alpha_1)|\varphi_{\alpha_2}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}+\right.\\
&+\varepsilon\delta(\gamma-\alpha_2)|\varphi_{\alpha_1}\varphi_{\alpha_3}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}+\\
&+\cdots+\\
&\left.+\varepsilon^{N-1}\delta(\gamma-\alpha_N)|\varphi_{\alpha_1}\cdots\varphi_{\alpha_{N-1}}\rangle^{(\varepsilon)}\right\}
\end{split}
\label{eq:131}
\end{align}
</mj>

如果构成$N$粒子态$\|\varphi\_{\alpha\_1}\cdots\varphi\_{\alpha\_N}\rangle^{(\varepsilon)}$的从$\|\varphi\_{\alpha\_1}\rangle$到$\|\varphi\_{\alpha\_N}\rangle$这些态中存在单粒子态$\|\varphi\_\gamma\rangle$，上式的结果就是一个$N-1$粒子态，其中不再含有$\|\varphi\_\gamma\rangle$，此即所谓$a\_\gamma$湮灭了一个处于$\|\varphi\_\gamma\rangle$态的粒子。若对称化的$N$粒子初态中不含$\|\varphi\_\gamma\rangle$，则$a\_\gamma$将整个初态湮灭掉。特别要注意这样一个特殊情况：

\begin{equation}
\label{eq:132}
a\_\gamma\|0\rangle=0
\end{equation}

湮灭算符的对易关系可以从式\eqref{eq:123}直接得到：

\begin{equation}
\label{eq:133}
[a\_{\alpha\_1},a\_{\alpha\_2}]\_{-\varepsilon}=-\varepsilon\left([a\_{\alpha\_1}^\dagger,a\_{\alpha\_2}^\dagger]\_{-\varepsilon}\right)^\dagger
\end{equation}

湮灭算符的对于玻色子是对易的（$\varepsilon=+$），对于费米子是反对易的（$\varepsilon=-$）:

\begin{equation}
\label{eq:134}
[a\_{\alpha\_1},a\_{\alpha\_2}]\_{-\varepsilon}=0
\end{equation}

此外还有第三条对易关系，例如，产生算符和湮灭算符之间的对易关系：

\begin{equation}
\label{eq:135}
[a\_{\alpha\_1},a\_{\alpha\_2}^\dagger]\_{-\varepsilon}=\delta(\alpha\_1-\alpha\_2)
\end{equation}

实际上，令$\|\varphi\_{\alpha\_1}\cdots\varphi\_{\alpha\_N}\rangle^{(\varepsilon)}$为$\mathcal{H}\_N^{(\varepsilon)}$中的任意基矢，有如下

<mj>
\begin{align}
\label{eq:136}
\begin{split}
a_\beta\left(a_\gamma^\dagger|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}\right)=&\sqrt{N+1}a_\beta|\varphi_\gamma\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}=\\
=&\delta(\beta-\gamma)|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}+\\
&+\varepsilon\delta(\beta-\alpha_1)|\varphi_\gamma\varphi_{\alpha_2}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}+\\
&+\cdots+\\
&+\varepsilon^N\delta(\beta-\alpha_N)|\varphi_\gamma\varphi_{\alpha_1}\cdots\varphi_{\alpha_{N-1}}\rangle^{(\varepsilon)}
\end{split}
\end{align}
</mj>

和

<mj>
\begin{align}
\label{eq:137}
\begin{split}
a_\gamma^\dagger\left(a_\beta|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}\right)=&\delta(\beta-\alpha_1)|\varphi_\gamma\varphi_{\alpha_2}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}+\\
&+\varepsilon\delta(\beta-\alpha_2)|\varphi_\gamma\varphi_{\alpha_1}\varphi_{\alpha_3}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}+\\
&+\cdots+\\
&+\varepsilon^{N-1}\delta(\beta-\alpha_N)|\varphi_\gamma\varphi_{\alpha_1}\cdots\varphi_{\alpha_{N-1}}\rangle^{(\varepsilon)}
\end{split}
\end{align}
</mj>

展开。

结合以上两式，便得到：

\begin{equation}
\label{eq:138}
\left(a\_\beta a\_\gamma^\dagger-\varepsilon a\_\gamma^\dagger a\_\beta\right)\|\varphi\_{\alpha\_1}\cdots\varphi\_{\alpha\_N}\rangle^{(\varepsilon)}=\delta(\beta-\gamma)\|\varphi\_{\alpha\_1}\cdots\varphi\_{\alpha\_N}\rangle^{(\varepsilon)}
\end{equation}

这就证明了式\eqref{eq:135}。

利用式\eqref{eq:120}和\eqref{eq:127}能够从真空态$\|0\rangle$构造任意$N$粒子态。湮灭算符对$\|0\rangle$的作用极其简单（见式\eqref{eq:132}）。通过式\eqref{eq:123}，\eqref{eq:134}和\eqref{eq:135}可以任意改变算符的作用次序。

但是，单单引入产生湮灭算符还不能充分体现其优势，除非能够将观察算符也形式化。

在任意观察算符$\widehat{A}$上使用完全性关系\eqref{eq:114}，首先得到：

<mj>
\begin{align}
\label{eq:139}
\begin{split}
\widehat{A}=&\mathbf{1}\cdot\widehat{A}\cdot\mathbf{1}=\\\
=&\int\cdots\int\mathrm{d}\alpha\_1\cdots\mathrm{d}\alpha_N\,\mathrm{d}\beta_1\cdots\mathrm{d}\beta_N|\varphi_{\alpha_1}\cdots\rangle^{(\varepsilon)}\cdot\\\
&\cdot{}^{(\varepsilon)}\langle\varphi_{\alpha_1}\cdots|\widehat{A}|\varphi_{\beta_1}\cdots\rangle^{(\varepsilon)}{}^{(\varepsilon)}\langle\varphi_{\beta_1}\cdots|
\end{split}
\end{align}
</mj>

将式\eqref{eq:120}和\eqref{eq:127}代入上式：

<mj>
\begin{align}
\begin{split}
\widehat{A}=&\frac{1}{N!}\int\cdots\int\mathrm{d}\alpha_1\cdots\mathrm{d}\alpha_N\,\mathrm{d}\beta_1\cdots\mathrm{d}\beta_N\,a_{\alpha_1}^\dagger\cdots a_{\alpha_N}^\dagger|0\rangle\cdot\\\
&\cdot{}^{(\varepsilon)}\langle\varphi_{\alpha_1}\cdots|\widehat{A}|\varphi_{\beta_1}\cdots\rangle^{(\varepsilon)}\langle0|a_{\beta_N}\cdots a_{\beta_1}
\end{split}
\label{eq:140}
\end{align}
</mj>

一般而言，$\widehat{A}$包含单体项和两体项：

<mj>
\begin{equation}
\label{eq:141}
\widehat{A}=\sum_{i=1}^n\widehat{A}_1^{(i)}+\frac{1}{2}\sum_{i,j}^{i\neq j}\widehat{A}_2^{(i,j)}
\end{equation}
</mj>

先讨论单体部分，需要得到式\eqref{eq:140}中的相应矩阵元：

<mj>
\begin{align}
\begin{split}
&{}^{(\varepsilon)}\langle\varphi_{\alpha_1}\cdots|\sum_{i=1}^n\widehat{A}_1^{(i)}|\varphi_{\beta_1}\cdots\rangle^{(\varepsilon)}=\\\
=&\frac{1}{N!}\sum_{\mathcal{P}_\beta}\varepsilon^{p_\beta}\mathcal{P}_\beta\left[\langle\varphi_{\alpha_1}^{(1)}|\widehat{A}_1^{(1)}|\varphi_{\beta_1}^{(1)}\rangle\langle\varphi_{\alpha_2}^{(2)}|\varphi_{\beta_2}^{(2)}\rangle\cdots\langle\varphi_{\alpha_N}^{(N)}|\varphi_{\beta_N}^{(N)}\rangle+\right.\\\
&+\cdots+\\\
&\left.+\langle\varphi_{\alpha_1}^{(1)}|\varphi_{\beta_1}^{(1)}\rangle\cdots\langle\varphi_{\alpha_N}^{(N)}|\widehat{A}_1^{(N)}|\varphi_{\beta_N}^{(N)}\rangle\right]
\end{split}
\label{eq:142}
\end{align}
</mj>

上式中用到了式\eqref{eq:109}。首先注意到，将上式代入\eqref{eq:140}后，每一个求和项（每个方括号内的总和）在置换后对求和作出相同的贡献。因为可以通过以下步骤将置换后的$\|\varphi\_{\beta\_i}^{(i)}\rangle$重新恢复标准排序：
1. 重新命名积分变量$\beta\_i$并
2. 交换相应的湮灭算符。

从\eqref{eq:134}可知第2步的交换会多出一个$\varepsilon^{p\_\beta}$因子，使得每个置换算符前的因数变成$\varepsilon^{2p\_\beta}=+1$。

同样，式\eqref{eq:142}方括号内的每一个求和项对式\eqref{eq:140}作出相同的贡献，可由此看出：
1. 交换相应的积分变量（$\alpha\_j\Leftrightarrow\alpha\_i,\beta\_j\Leftrightarrow\beta\_i$）并
2. 重排相应数目的产生湮灭算符。

第2步中的每种情形产生一个因子$(\varepsilon^2)^{n\_j}$。由此得到一个大大简化的中间结果：

<mj>
\begin{align}
\begin{split}
\sum_{i=1}^n\widehat{A}_1^{(i)}=&\frac{N}{N!}\int\cdots\int\mathrm{d}\alpha_1\cdots\mathrm{d}\beta_N\,a_{\alpha_1}^\dagger\cdots a_{\alpha_N}^\dagger|0\rangle\cdot\\\
&\cdot\left\{\langle\varphi_{\alpha_1}^{(1)}|\widehat{A}_1^{(1)}|\varphi_{\beta_1}^{(1)}\rangle\delta(\alpha_2-\beta_2)\cdots\delta(\alpha_N-\beta_N)\right\}\cdot\\\
&\cdot\langle0|a_{\beta_N}\cdots a_{\beta_1}=\\\
=&\iint\mathrm{d}\alpha_1\,\mathrm{d}\beta_1\langle\varphi_{\alpha_1}^{(1)}|\widehat{A}_1^{(1)}|\varphi_{\beta_1}^{(1)}\rangle a_{\alpha_1}^\dagger\cdot\\\
&\cdot\left\{\frac{1}{(N-1)!}\int\cdots\int\mathrm{d}\alpha_2\cdots\mathrm{d}\alpha_N\,a_{\alpha_2}^\dagger\cdots a_{\alpha_N}^\dagger|0\rangle\langle0|a_{\alpha_N}\cdots a_{\alpha_2}\right\}a_{\beta_1}
\end{split}
\label{eq:143}
\end{align}
</mj>

从式\eqref{eq:114}可见，上式最后的花括号中其实是$\mathcal{H}\_{N-1}^{(\varepsilon)}$中的单位元$\mathbf{1}$。故最终结果就是：

\begin{equation}
\label{eq:144}
\sum\_{i=1}^n\widehat{A}\_1^{(i)}=\iint\mathrm{d}\alpha\,\mathrm{d}\beta\langle\varphi\_{\alpha}\|\widehat{A}\_1\|\varphi\_{\beta}\rangle a\_{\alpha}^\dagger a\_{\beta}
\end{equation}

上式右边不显含粒子数$N$，其实它隐含在单位元中了，事实上由\eqref{eq:143}可以想见它就在$a\_{\alpha}^\dagger$和$a\_{\beta}$之间。

同理可得观察算符$\widehat{A}$的两体项：

<mj>
\begin{align}
\label{eq:145}
\begin{split}
\frac{1}{2}\sum_{i,j}^{i\neq j}\widehat{A}_2^{(i,j)}=&\frac{1}{2N!}\int\cdots\int\mathrm{d}\alpha_1\cdots\mathrm{d}\beta_N\,a_{\alpha_1}^\dagger\cdots a_{\alpha_N}^\dagger|0\rangle\cdot\\\
&\cdot\left\{\frac{1}{N!}\sum_{\mathcal{P}_\beta}\varepsilon^{p_\beta}\mathcal{P}_\beta\left[\langle\varphi_{\alpha_1}^{(1)}|\langle\varphi_{\alpha_2}^{(2)}|\widehat{A}_2^{(1,2)}|\varphi_{\beta_1}^{(1)}\rangle|\varphi_{\beta_2}^{(2)}\rangle\cdot\right.\right.\\\
&\cdot\langle\varphi_{\alpha_3}^{(3)}|\varphi_{\beta_3}^{(3)}\rangle\cdots\langle\varphi_{\alpha_N}^{(N)}|\varphi_{\beta_N}^{(N)}\rangle+\\\
&+\langle\varphi_{\alpha_1}^{(1)}|\langle\varphi_{\alpha_3}^{(3)}|\widehat{A}_2^{(1,3)}|\varphi_{\beta_1}^{(1)}\rangle|\varphi_{\beta_3}^{(3)}\rangle\langle\varphi_{\alpha_2}^{(2)}|\varphi_{\beta_2}^{(2)}\rangle\cdot\\\
&\left.\left.\cdot\langle\varphi_{\alpha_4}^{(4)}|\varphi_{\beta_4}^{(4)}\rangle\cdots\langle\varphi_{\alpha_N}^{(N)}|\varphi_{\beta_N}^{(N)}\rangle+\cdots\right]\right\}\langle0|a_{\beta_N}\cdots a_{\beta_1}
\end{split}
\end{align}
</mj>

和前面单体项完全相同的论证可以证明，$N!$个置换算符$\mathcal{P}\_\beta$作用项对多重积分贡献一样，并且每个方括号中$N(N-1)$个求和项相等。于是：

<mj>
\begin{align}
\label{eq:146}
\begin{split}
\frac{1}{2}\sum_{i,j}^{i\neq j}\widehat{A}_2^{(i,j)}=&\frac{1}{2}\int\cdots\int\mathrm{d}\alpha_1\,\mathrm{d}\alpha_2\,\mathrm{d}\beta_1\,\mathrm{d}\beta_2\langle\varphi_{\alpha_1}\varphi_{\alpha_2}|\widehat{A}_2^{(1,2)}|\varphi_{\beta_1}\varphi_{\beta_2}\rangle\cdot\\\
&\cdot a_{\alpha_1}^\dagger a_{\alpha_2}^\dagger\left\{\frac{1}{(N-2)!}\int\cdots\int\mathrm{d}\alpha_3\cdots\mathrm{d}\alpha_N\cdot\right.\\\
&\left.\cdot a_{\alpha_3}^\dagger\cdots a_{\alpha_N}^\dagger|0\rangle\langle0|a_{\alpha_N}\cdots a_{\alpha_3}\right\}a_{\beta_2}a_{\beta_1}
\end{split}
\end{align}
</mj>

上式花括号中其实是$\mathcal{H}\_{N-2}^{(\varepsilon)}$中的单位元$\mathbf{1}$，由此可得：

\begin{equation}
\label{eq:147}
\frac{1}{2}\sum\_{i,j}^{i\neq j}\widehat{A}\_2^{(i,j)}=\frac{1}{2}\int\cdots\int\mathrm{d}\alpha\,\mathrm{d}\beta\,\mathrm{d}\gamma\,\mathrm{d}\delta\langle\varphi\_\alpha\varphi\_\beta\|\widehat{A}\_2\|\varphi\_\gamma\varphi\_\delta\rangle a\_\alpha^\dagger a\_\beta^\dagger a\_\delta a\_\gamma
\end{equation}

矩阵元可由非对称化态矢构造：

\begin{equation}
\label{eq:148}
\langle\varphi\_\alpha\varphi\_\beta\|\widehat{A}\_2\|\varphi\_\gamma\varphi\_\delta\rangle=\langle\varphi\_\alpha^{(1)}\|\langle\varphi\_\beta^{(2)}\|\widehat{A}\_2^{(1,2)}\|\varphi\_\gamma^{(1)}\|\varphi\_\delta^{(2)}\rangle
\end{equation}

也可由对称化态矢构造：

\begin{equation}
\label{eq:149}
\|\varphi\_\gamma\varphi\_\delta\rangle^{(\varepsilon)}=\frac{1}{2!}\left(\|\varphi\_\gamma^{(1)}\|\varphi\_\delta^{(2)}\rangle+\varepsilon\|\varphi\_\gamma^{(1)}\|\varphi\_\delta^{(2)}\rangle\right)
\end{equation}

实际上，可由此验证：

<mj>
\begin{align}
\label{eq:150}
\begin{split}
{}^{(\varepsilon)}\langle\varphi_\alpha\varphi_\beta|\widehat{A}_2|\varphi_\gamma\varphi_\delta\rangle^{(\varepsilon)}=&\frac{1}{4}\left\{\langle\varphi_\alpha^{(1)}|\langle\varphi_\beta^{(2)}|\widehat{A}_2^{(1,2)}|\varphi_\gamma^{(1)}|\varphi_\delta^{(2)}\rangle+\right.\\\
&+\varepsilon\langle\varphi_\alpha^{(1)}|\langle\varphi_\beta^{(2)}|\widehat{A}_2^{(1,2)}|\varphi_\gamma^{(2)}|\varphi_\delta^{(1)}\rangle+\\\
&+\varepsilon\langle\varphi_\alpha^{(2)}|\langle\varphi_\beta^{(1)}|\widehat{A}_2^{(1,2)}|\varphi_\gamma^{(1)}|\varphi_\delta^{(2)}\rangle+\\\
&\left.+\varepsilon^2\langle\varphi_\alpha^{(2)}|\langle\varphi_\beta^{(1)}|\widehat{A}_2^{(1,2)}|\varphi_\gamma^{(2)}|\varphi_\delta^{(1)}\rangle\right\}
\end{split}
\end{align}
</mj>

上式中的每一个求和项对\eqref{eq:147}贡献相同，归一化因子保证了在\eqref{eq:147}中使用对称化矩阵元与非对称化的效果相同，可便宜行事。

现在做个小结。通过式\eqref{eq:120}和\eqref{eq:127}将产生算符连续作用于真空态$\|0\rangle$构造$N$粒子态的方式免去了由单粒子态乘积构造对称（反对称）态的繁冗，而且操作起来很简单。态矢的对称性特征完全由三个基本对易关系\eqref{eq:123}，\eqref{eq:134}和\eqref{eq:135}承载。$N$粒子态的观察算符也能由产生湮灭算符构造，只消由\eqref{eq:144}和\eqref{eq:147}直接计算余下的矩阵元。

现在介绍两个特殊的算符：占有密度算符和粒子数算符。

首先是占有密度算符：

\begin{equation}
\label{eq:151}
\hat{n}\_\alpha=a\_\alpha^\dagger a\_\alpha
\end{equation}

此算符的作用可根据\eqref{eq:119}和\eqref{eq:131}得到：

<mj>
\begin{align}
\label{eq:152}
\begin{split}
\hat{n}_\alpha|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}=&\delta(\alpha-\alpha_1)|\varphi_\alpha\varphi_{\alpha_2}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}+\\\
&+\varepsilon\delta(\alpha-\alpha_2)|\varphi_\alpha\varphi_{\alpha_1}\varphi_{\alpha_3}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}+\\\
&+\cdots+\\\
&+\varepsilon^{N-1}\delta(\alpha-\alpha_N)|\varphi_\alpha\varphi_{\alpha_1}\cdots\varphi_{\alpha_{N-1}}\rangle^{(\varepsilon)}=\\\
=&\delta(\alpha-\alpha_1)|\varphi_\alpha\varphi_{\alpha_2}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}+\\\
&+\varepsilon\delta(\alpha-\alpha_2)\varepsilon|\varphi_{\alpha_1}\varphi_\alpha\varphi_{\alpha_3}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}+\\\
&+\cdots+\\\
&+\varepsilon^{N-1}\delta(\alpha-\alpha_N)\varepsilon^{N-1}|\varphi_{\alpha_1}\cdots\varphi_{\alpha_{N-1}}\varphi_\alpha\rangle^{(\varepsilon)}
\end{split}
\end{align}
</mj>

可见$\mathcal{H}\_N^{(\varepsilon)}$的基矢是占有密度算符的本征矢：

\begin{equation}
\label{eq:153}
\hat{n}\_\alpha\|\varphi\_{\alpha\_1}\cdots\varphi\_{\alpha\_N}\rangle^{(\varepsilon)}=\left\\{\sum\_{i=1}^{n}\delta(\alpha-\alpha\_i)\right\\}\|\varphi\_{\alpha\_1}\cdots\varphi\_{\alpha\_N}\rangle^{(\varepsilon)}
\end{equation}

上式用到了$\delta$函数的挑选性。花括号中的即是微观占有密度。

其次是粒子数算符：

\begin{equation}
\label{eq:154}
\widehat{N}=\int\mathrm{d}\alpha\,\hat{n}\_\alpha=\int\mathrm{d}\alpha\,a\_\alpha^\dagger a\_\alpha
\end{equation}

从式\eqref{eq:153}可见$\mathcal{H}\_N^{(\varepsilon)}$也是$\widehat{N}$的本征矢，其本征值就是总粒子数$N$：

<mj>
\begin{align}
\label{eq:155}
\begin{split}
\widehat{N}|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}&=\int\mathrm{d}\alpha\sum_{i=1}^{N}\delta(\alpha-\alpha_i)|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}=\\\
&=N|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}
\end{split}
\end{align}
</mj>

利用产生湮灭算符的基本对易关系可得如下对易子：

<mj>
\begin{align}
\label{eq:156}
\begin{split}
\left[\hat{n}_\alpha,a_\beta^\dagger\right]_-&=\hat{n}_\alpha a_\beta^\dagger-a_\beta^\dagger\hat{n}_\alpha=\\\
&=a_\alpha^\dagger a_\alpha a_\beta^\dagger-a_\beta^\dagger\hat{n}_\alpha=\\\
&=a_\alpha^\dagger\left(\delta(\alpha-\beta)+\varepsilon a_\beta^\dagger a_\alpha\right)-a_\beta^\dagger\hat{n}_\alpha=\\\
&=a_\alpha^\dagger\delta(\alpha-\beta)+\varepsilon^2a_\beta^\dagger a_\alpha^\dagger a_\alpha-a_\beta^\dagger\hat{n}_\alpha
\end{split}
\end{align}
</mj>

上式最后两项相消，得到：

\begin{equation}
\label{eq:157}
\left[\hat{n}\_\alpha,a\_\beta^\dagger\right]\_-=a\_\alpha^\dagger\delta(\alpha-\beta)
\end{equation}

同理可得：

\begin{equation}
\label{eq:158}
\left[\hat{n}\_\alpha,a\_\beta\right]\_-=-a\_\alpha\delta(\alpha-\beta)
\end{equation}

由\eqref{eq:154}可得到对于粒子数算符的类似关系式：

<mj>
\begin{align}
\left[\widehat{N},a_\alpha^\dagger\right]_-&=a_\alpha^\dagger\label{eq:159}\\\
\left[\widehat{N},a_\alpha\right]_-&=-a_\alpha\label{eq:160}
\end{align}
</mj>

也可写成如下形式：

<mj>
\begin{align}
\widehat{N}a_\alpha^\dagger&=a_\alpha^\dagger\left(\widehat{N}+\mathbf{1}\right)\label{eq:161}\\\
\widehat{N}a_\alpha&=a_\alpha\left(\widehat{N}-\mathbf{1}\right)\label{eq:162}
\end{align}
</mj>

将其作用于基矢：

<mj>
\begin{align}
\widehat{N}\left(a_\alpha^\dagger|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}\right)&=(N+1)\left(a_\alpha^\dagger|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}\right)\label{eq:163}\\\
\widehat{N}\left(a_\alpha|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}\right)&=(N-1)\left(a_\alpha|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}\right)\label{eq:164}
\end{align}
</mj>

由此可见$a\_\alpha^\dagger$叫做产生算符而$a\_\alpha$叫做湮灭算符真是恰如其分。

之前假设单粒子观察算符$\widehat{\varphi}$的本征谱是离散的，并由其本征矢构成$N$粒子希尔伯特空间$\mathcal{H}\_N^{(\varepsilon)}$的本征矢。此类观察算符的一个重要例子就是位置算符$\hat{r}$，相应的产生湮灭算符记作场算符$\widehat{\psi}^\dagger(\mathbf{r})$和$\widehat{\psi}(\mathbf{r})$。之前导出的诸关系式对这些算符自然也成立，不过记号稍有不同：

<mj>
\begin{align}
\widehat{\psi}^\dagger(\mathbf{r})|\mathbf{r}_1\cdots\mathbf{r}_N\rangle^{(\varepsilon)}&=\sqrt{N+1}|\mathbf{r}\mathbf{r}_1\cdots\mathbf{r}_N\rangle^{(\varepsilon)}\label{eq:165}\\\
|\mathbf{r}_1\cdots\mathbf{r}_N\rangle^{(\varepsilon)}&=\frac{1}{\sqrt{N!}}\widehat{\psi}^\dagger(\mathbf{r}_1)\cdots\widehat{\psi}^\dagger(\mathbf{r}_N)|0\rangle\label{eq:166}
\end{align}
</mj>

场算符的基本对易关系可直接从\eqref{eq:123}，\eqref{eq:134}和\eqref{eq:135}得到：

<mj>
\begin{align}
\left[\widehat{\psi}^\dagger(\mathbf{r}),\widehat{\psi}^\dagger(\mathbf{r}')\right]_{-\varepsilon}&=0\label{eq:167}\\\
\left[\widehat{\psi}(\mathbf{r}),\widehat{\psi}(\mathbf{r}')\right]_{-\varepsilon}&=0\label{eq:168}\\\
\left[\widehat{\psi}(\mathbf{r}),\widehat{\psi}^\dagger(\mathbf{r}')\right]_{-\varepsilon}&=\delta(\mathbf{r}-\mathbf{r}')\label{eq:169}
\end{align}
</mj>

它们和广义的产生湮灭算符<mj>$a_\alpha^\dagger$和$a_\alpha$</mj>间的联系也很重要。完全性关系表明：

<mj>
\begin{equation}
\label{eq:170}
|\varphi_\alpha\rangle=\int\mathrm{d}^3r|\mathbf{r}\rangle\langle\mathbf{r}|\varphi_\alpha\rangle=\int\mathrm{d}^3r\,\varphi_\alpha(\mathbf{r})|\mathbf{r}\rangle
\end{equation}
</mj>

再根据<mj>$|\varphi_\alpha\rangle=a_\alpha^\dagger|0\rangle$</mj>和<mj>$|\mathbf{r}\rangle=\widehat{\psi}^\dagger(\mathbf{r})|0\rangle$</mj>得到：

<mj>
\begin{align}
\label{eq:171}
a_\alpha^\dagger&=\int\mathrm{d}^3r\,\varphi_\alpha(\mathbf{r})\widehat{\psi}^\dagger(\mathbf{r})\\\
\label{eq:172}
a_\alpha&=\int\mathrm{d}^3r\,\varphi_\alpha^*(\mathbf{r})\widehat{\psi}(\mathbf{r})
\end{align}
</mj>

注意$\widehat{\psi}^\dagger(\mathbf{r})$和$\widehat{\psi}(\mathbf{r})$是算符，而<mj>$\varphi_\alpha(\mathbf{r})$</mj>是态矢<mj>$|\varphi_\alpha\rangle$</mj>的标量波函数。式\eqref{eq:171}和\eqref{eq:172}的逆可通过

<mj>
\begin{equation}
\label{eq:173}
|\mathbf{r}\rangle=\int\mathrm{d}\alpha|\varphi_\alpha\rangle\langle\varphi_\alpha|\mathbf{r}\rangle
\end{equation}
</mj>

由同样的方式得到：
<mj>
\begin{align}
\label{eq:174}
\widehat{\psi}^\dagger(\mathbf{r})&=\int\mathrm{d}\alpha\,\varphi_\alpha^*(\mathbf{r})a_\alpha^\dagger\\\
\label{eq:175}
\widehat{\psi}(\mathbf{r})&=\int\mathrm{d}\alpha\,\varphi_\alpha(\mathbf{r})a_\alpha
\end{align}
</mj>

### 5.2 “离散的”福克表象
这里也是用单粒子观察算符$\widehat{\varphi}$的本征矢来构造$N$粒子体系的希尔伯特空间$\mathcal{H}\_N^{(\varepsilon)}$的基矢，只是此处的$\widehat{\varphi}$的本征谱是离散的：

<mj>
\begin{align}
\label{eq:176}
\langle\varphi_\beta|\varphi_\alpha\rangle&=\varphi_\alpha|\varphi_\alpha\rangle\\\
\label{eq:177}
\langle\varphi_\alpha|\varphi_\beta\rangle&=\delta_{\alpha\beta}\\\
\label{eq:178}
\sum_\alpha|\varphi_\alpha\rangle\langle\varphi_\alpha|&=\mathbf{1}\quad\text{in }\mathcal{H}_1
\end{align}
</mj>

理论上，借鉴[5.1](#51-连续的福克表象)中的处理方式能使得此处的推导更加顺利。

出发点还是\eqref{eq:104}中的非对称化的$N$粒子态：

\begin{equation}
\label{eq:179}
\|\varphi\_{\alpha\_1}\cdots\varphi\_{\alpha\_N}\rangle=\|\varphi\_{\alpha\_1}^{(1)}\rangle\|\varphi\_{\alpha\_2}^{(2)}\rangle\cdots\|\varphi\_{\alpha\_N}^{(N)}\rangle
\end{equation}

此处的态指标$\alpha\_1,\cdots,\alpha\_N$依然是一个任意的标准排序。将式\eqref{eq:56}中的$\widehat{S}\_\varepsilon$作用在这个态上得到对称化（反对称化）的$N$粒子态：

\begin{equation}
\label{eq:180}
\|\varphi\_{\alpha\_1}\cdots\varphi\_{\alpha\_N}\rangle^{(\varepsilon)}=C\_\varepsilon\sum\_\mathcal{P}\varepsilon^p\mathcal{P}\|\varphi\_{\alpha\_1}\cdots\varphi\_{\alpha\_N}\rangle
\end{equation}

与\eqref{eq:105}的差别只是一个待定的归一化常数$C\_\varepsilon$。对于费米子（$\varepsilon=-$）反对称化的态矢可写成行列式形式：

<mj>
\begin{equation}
\label{eq:181}
|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(-)}=C_-
\begin{vmatrix}
|\varphi_{\alpha_1}^{(1)}\rangle & |\varphi_{\alpha_1}^{(2)}\rangle & \cdots & |\varphi_{\alpha_1}^{(N)}\rangle\\\
|\varphi_{\alpha_2}^{(1)}\rangle & |\varphi_{\alpha_2}^{(2)}\rangle & \cdots & |\varphi_{\alpha_2}^{(N)}\rangle\\\
\vdots & \vdots & \ddots & \vdots \\\
|\varphi_{\alpha_N}^{(1)}\rangle & |\varphi_{\alpha_N}^{(2)}\rangle & \cdots & |\varphi_{\alpha\_N}^{(N)}\rangle\\\
\end{vmatrix}
\end{equation}
</mj>

这就是所谓的斯莱特行列式。

当$N$粒子态中两组量子数相同时（$\alpha\_i=\alpha\_j$），行列式就有相同的两行，行列式为零。这意味着不会有两个费米子处于同一单粒子态，此即泡利不相容原理。当然这不仅限于离散本征谱的情形，\eqref{eq:105}（$\varepsilon=-$）自然也能写成斯莱特行列式。

接着来确定归一化常数$C\_\varepsilon$并引入占有数$n\_i$。这些数反映了某个单粒子态$\|\varphi\_{\alpha\_i}\rangle$在$N$粒子态$\|\varphi\_{\alpha\_1}\cdots\rangle^{(\varepsilon)}$中出现的频率，或者，更直观一点，处于态$\|\varphi\_{\alpha\_i}\rangle$的全同粒子的数目：

<mj>
\begin{align}
\label{eq:182}
\begin{split}
\sum_i n_i&=N&\\
n_i&=0,1&\text{Fermions}\\
n_i&=0,1,2,\ldots&\quad\text{Bosons}\\
\end{split}
\end{align}
</mj>

限定$C\_\varepsilon$为实数，归一化意味着：

<mj>
\begin{align}
\label{eq:183}
\begin{split}
1\equiv\langle\varphi_N^{(\varepsilon)}|\varphi_N^{(\varepsilon)}\rangle&=C_\varepsilon\sum_\mathcal{P}\varepsilon^p\langle\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}|\mathcal{P}^\dagger|\varphi_N^{(\varepsilon)}\rangle\overset{(\mathcal{P}^\dagger=\mathcal{P})}{=}\\\
&\hspace{-0.85em}\overset{(\mathcal{P}^\dagger=\mathcal{P})}{=}C_\varepsilon\sum_\mathcal{P}\varepsilon^{2p}\langle\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}|\varphi_N^{(\varepsilon)}\rangle=\\\
&=N!C_\varepsilon\langle\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}|\varphi_N^{(\varepsilon)}\rangle
\end{split}
\end{align}
</mj>

于是：

\begin{equation}
\label{eq:184}
(N!C\_\varepsilon^2)^{-1}=\sum\_\mathcal{P}\varepsilon^p\langle\varphi\_{\alpha\_1}^{(1)}\|\langle\varphi\_{\alpha\_2}^{(2)}\|\cdots\langle\varphi\_{\alpha\_N}^{(N)}\|\left(\mathcal{P}\|\varphi\_{\alpha\_1}^{(1)}\rangle\|\varphi\_{\alpha\_2}^{(2)}\rangle\cdots\|\varphi\_{\alpha\_N}^{(N)}\rangle\right)
\end{equation}

对于费米子体系，每个态有且仅有一次出现，任何两个态都不相同。上式右边仅当$\mathcal{P}$是单位算符时才不为零，由$\varepsilon^0=1$及式\eqref{eq:177}可见右边等于$1$。因此：

\begin{equation}
\label{eq:185}
C\_-=\frac{1}{\sqrt{N!}}
\end{equation}

对于玻色子体系（$\varepsilon=+$），允许存在相同的单粒子态$\|\varphi\_{\alpha\_i}\rangle$，在这$n\_i$个态之间置换粒子，总计有

\begin{equation}
\label{eq:186}
n\_1!n\_2!\cdots n\_i!\cdots
\end{equation}

个这样的置换，每个都对\eqref{eq:184}贡献值为$+1$的求和项，于是：

\begin{equation}
\label{eq:187}
C\_+=\left(N!\prod\_i n\_i!\right)^{-1/2}
\end{equation}

这个形式对费米子一样适用，因为$0!=1!=1$。

可见一个$N$粒子态被它的占有数唯一确定。由此导致另一种表象：占有数表象。

<mj>
\begin{align}
\label{eq:188}
\begin{split}
&|N;n_1n_2\cdots n_i\cdots n_j\cdots\rangle^{(\varepsilon)}\equiv|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}=\\\
&=C_\varepsilon\sum_\mathcal{P}\varepsilon^p\mathcal{P}\left\{\underbrace{|\varphi_{\alpha_1}^{(1)}\rangle|\varphi_{\alpha_1}^{(2)}\rangle\cdots}_{n_1}\cdots\underbrace{|\varphi_{\alpha_i}^{(p)}\rangle|\varphi_{\alpha_i}^{(p+1)}\rangle\cdots}_{n_i}\cdots\right\}
\end{split}
\end{align}
</mj>

全部占有数都在这个态矢符号中出现，如果某个单粒子态未被占据，就用$n\_i=0$标记。当且仅当两个态矢的所有占有数都一致才是相同的态。从单粒子态可直接导出正交关系：

\begin{equation}
\label{eq:189}
{}^{(\varepsilon)}\langle N;\cdots n\_i\cdots\|\overline{N};\cdots\bar{n}\_i\cdots\rangle^{(\varepsilon)}=\delta\_{N\overline{N}}\prod\_i\delta\_{n\_i\bar{n}\_i}
\end{equation}

对这个所谓的福克态同样有完全性关系：

\begin{equation}
\label{eq:190}
\sum\_{n\_1}\sum\_{n\_2}\cdots\sum\_{n\_i}\cdots\|N;\cdots n\_i\cdots\rangle^{(\varepsilon)}{}^{(\varepsilon)}\langle N;\cdots n\_i\cdots\|=\mathbf{1}
\end{equation}

上式对所有满足$\sum\_i n\_i=N$的占有数进行求和。

和[5.1](#51-连续的福克表象)中一样，产生湮灭算符根据归一化因子定义。产生算符$a\_{\alpha\_r}^\dagger\equiv a\_r^\dagger$：

<mj>
\begin{align}
\label{eq:191}
\begin{split}
&a_r^\dagger|N;\cdots n_r\cdots\rangle^{(\varepsilon)}=\\\
&=a_r^\dagger|\varphi_{\alpha_1}\cdots\varphi_{\alpha_N}\rangle^{(\varepsilon)}\equiv\\\
&\equiv\sqrt{n_r+1}\left|\varphi_{\alpha_r}\underbrace{\varphi_{\alpha_1}\varphi_{\alpha_1}\cdots}_{n_1}\cdots\underbrace{\varphi_{\alpha_r}\varphi_{\alpha_r}\cdots}_{n_r}\cdots\right\rangle^{(\varepsilon)}=\\\
&=\varepsilon^{N_r}\sqrt{n_r+1}\left|\underbrace{\varphi_{\alpha_1}\varphi_{\alpha_1}\cdots}_{n_1}\cdots\underbrace{\varphi_{\alpha_r}\varphi_{\alpha_r}\cdots}_{n_r+1}\cdots\right\rangle^{(\varepsilon)}
\end{split}
\end{align}
</mj>

这里，

\begin{equation}
\label{eq:192}
N\_r=\sum\_{i=1}^{r-1}n\_i
\end{equation}

是恢复标准排列所需的交换次数。产生算符对玻色子（$\varepsilon=+$）和费米子（$\varepsilon=-$）的作用如下：

<mj>
\begin{align}
\label{eq:193}
a_r^\dagger|N;\cdots n_r\cdots\rangle^{(+)}&=\sqrt{n_r+1}|N+1;\cdots n_r+1\cdots\rangle^{(+)}\\
\label{eq:194}
a_r^\dagger|N;\cdots n_r\cdots\rangle^{(-)}&=(-1)^{N_r}\delta_{n_r,0}|N+1;\cdots n_r+1\cdots\rangle^{(-)}\\
\end{align}
</mj>

每个$N$粒子福克态都可以通过反复对真空态作用产生算符得到：

\begin{equation}
\label{eq:195}
\|N;\cdots n\_i\cdots\rangle^{(\varepsilon)}=\prod\_{p=1\cdots}^{\sum n\_p=N}\frac{(a\_p^\dagger)^{n\_p}}{\sqrt{n\_p!}}\varepsilon^{N\_p}\|0\rangle
\end{equation}

同样，由产生算符的共轭定义湮灭算符$a\_r\equiv(a\_r^\dagger)^\dagger$，从下面的矩阵元可见其作用：

<mj>
\begin{align}
\label{eq:196}
\begin{split}
&{}^{(\varepsilon)}\langle N;\cdots n_r\cdots|a_r|\overline{N};\cdots\bar{n}_r\cdots\rangle^{(\varepsilon)}=\\\
&=\varepsilon^{N_r}\sqrt{n_r+1}{}^{(\varepsilon)}\langle N+1;\cdots n_r+1\cdots|\overline{N};\cdots\bar{n}_r\cdots\rangle^{(\varepsilon)}=\\\
&=\varepsilon^{N_r}\sqrt{n_r+1}\delta_{N+1,\overline{N}}(\delta_{n_1,\bar{n}_1}\cdots\delta_{n_r+1,\bar{n}_r}\cdots)=\\\
&=\varepsilon^{\overline{N}_r}\sqrt{\bar{n}_r}\delta_{N,\overline{N}-1}(\delta_{n_1,\bar{n}_1}\cdots\delta_{n_r,\bar{n}_r-1}\cdots)=\\\
&=\varepsilon^{\overline{N}_r}\sqrt{\bar{n}_r}{}^{(\varepsilon)}\langle N;n_1\cdots n_r\cdots|\overline{N}-1;\bar{n}_1\cdots\bar{n}_r-1\cdots\rangle^{(\varepsilon)}
\end{split}
\end{align}
</mj>

上式第四行用到了$\delta$函数的挑选性。由于基矢是任意的，便得到如下关系：

\begin{equation}
\label{eq:197}
a\_r\|\overline{N};\cdots\bar{n}\_r\cdots\rangle^{(\varepsilon)}=\varepsilon^{\overline{N}\_r}\sqrt{\bar{n}\_r}\|\overline{N}-1;\bar{n}\_1\cdots\bar{n}\_r-1\cdots\rangle^{(\varepsilon)}
\end{equation}

湮灭算符对玻色子（$\varepsilon=+$）和费米子（$\varepsilon=-$）的作用如下：

<mj>
\begin{align}
\label{eq:198}
a_r|N;\cdots n_r\cdots\rangle^{(+)}&=\sqrt{n_r}|N-1;\cdots n_r-1\cdots\rangle^{(+)}\\\
\label{eq:199}
a_r|N;\cdots n_r\cdots\rangle^{(-)}&=\delta_{n_r,1}(-1)^{N_r}|N-1;\cdots n_r-1\cdots\rangle^{(-)}\\\
\end{align}
</mj>

从定义式\eqref{eq:193}\eqref{eq:194}和\eqref{eq:198}\eqref{eq:199}可以导出基本对易关系：

1\. 玻色子（$r\neq p$）：

<mj>
\begin{align}
&\begin{split}
a_r^\dagger a_p^\dagger&|\cdots n_r\cdots n_p\cdots\rangle^{(+)}=\\\
&=\sqrt{n_r+1}\sqrt{n_p+1}|\cdots n_r+1\cdots n_p+1\cdots\rangle^{(+)}=\\\
&=a_p^\dagger a_r^\dagger|\cdots n_r\cdots n_p\cdots\rangle^{(+)}
\end{split}\label{eq:200}\\\
&\begin{split}
a_r a_p&|\cdots n_r\cdots n_p\cdots\rangle^{(+)}=\\\
&=\sqrt{n_r}\sqrt{n_p}|\cdots n_r-1\cdots n_p-1\cdots\rangle^{(+)}=\\\
&=a_p a_r|\cdots n_r\cdots n_p\cdots\rangle^{(+)}
\end{split}\label{eq:201}\\\
&\begin{split}
a_r^\dagger a_p&|\cdots n_r\cdots n_p\cdots\rangle^{(+)}=\\\
&=\sqrt{n_r+1}\sqrt{n_p}|\cdots n_r+1\cdots n_p-1\cdots\rangle^{(+)}=\\\
&=a_p a_r^\dagger|\cdots n_r\cdots n_p\cdots\rangle^{(+)}
\end{split}\label{eq:202}\\\
&\begin{split}
a_r^\dagger a_r&|\cdots n_r\cdots\rangle^{(+)}=\\\
&=\sqrt{n_r}a_r^\dagger|\cdots n_r-1\cdots\rangle^{(+)}=\\\
&=n_r|\cdots n_r\cdots\rangle^{(+)}
\end{split}\label{eq:203}\\\
&\begin{split}
a_r a_r^\dagger&|\cdots n_r\cdots\rangle^{(+)}=\\\
&=\sqrt{n_r+1}a_r|\cdots n_r+1\cdots\rangle^{(+)}=\\\
&=(n_r+1)|\cdots n_r\cdots\rangle^{(+)}
\end{split}\label{eq:204}
\end{align}
</mj>

2\. 费米子（$r<p$）：

<mj>
\begin{align}
&\begin{split}
a_r^\dagger a_p^\dagger&|\cdots n_r\cdots n_p\cdots\rangle^{(-)}=\\\
&=(-1)^{N_r}(-1)^{N_p}\delta_{n_r,0}\delta_{n_p,0}|\cdots n_r+1\cdots n_p+1\cdots\rangle^{(-)}
\end{split}\label{eq:205}\\\
&\begin{split}
a_p^\dagger a_r^\dagger&|\cdots n_r\cdots n_p\cdots\rangle^{(-)}=\\\
&=(-1)^{N_p+1}(-1)^{N_r}\delta_{n_p,0}\delta_{n_r,0}|\cdots n_r+1\cdots n_p+1\cdots\rangle^{(-)}=\\\
&=-a_r^\dagger a_p^\dagger|\cdots n_r\cdots n_p\cdots\rangle^{(-)}
\end{split}\label{eq:206}\\\
&\begin{split}
a_r^\dagger a_r&|\cdots n_r\cdots\rangle^{(-)}=\\\
&=(-1)^{2N_r}\delta_{n_r,1}|\cdots n_r\cdots\rangle^{(-)}=\delta_{n_r,1}|\cdots n_r\cdots\rangle^{(-)}
\end{split}\label{eq:207}\\\
&\begin{split}
a_r a_r^\dagger&|\cdots n_r\cdots\rangle^{(-)}=\\\
&=(-1)^{2N_r}\delta_{n_r,0}|\cdots n_r\cdots\rangle^{(-)}=\delta_{n_r,0}|\cdots n_r\cdots\rangle^{(-)}
\end{split}\label{eq:208}\\\
&\begin{split}
a_r^\dagger a_p&|\cdots n_r\cdots n_p\cdots\rangle^{(-)}=\\\
&=(-1)^{N_r}(-1)^{N_p}\delta_{n_r,0}\delta_{n_p,1}|\cdots n_r+1\cdots n_p-1\cdots\rangle^{(-)}
\end{split}\label{eq:209}\\\
&\begin{split}
a_p a_r^\dagger&|\cdots n_r\cdots n_p\cdots\rangle^{(-)}=\\\
&=(-1)^{N_p+1}(-1)^{N_r}\delta_{n_p,1}\delta_{n_r,0}|\cdots n_r+1\cdots n_p-1\cdots\rangle^{(-)}=\\\
&=-a_r^\dagger a_p|\cdots n_r\cdots n_p\cdots\rangle^{(-)}
\end{split}\label{eq:210}
\end{align}
</mj>

因为上述关系对任意基矢都适用，所以有如下算符恒等式：

<mj>
\begin{align}
\label{eq:211}
[a_r,a_s]_{-\varepsilon}&=0\\
\label{eq:212}
[a_r^\dagger,a_s^\dagger]_{-\varepsilon}&=0\\
\label{eq:213}
[a_r,a_s^\dagger]_{-\varepsilon}&=\delta_{rs}\\
\end{align}
</mj>

这些就是离散福克表象中类似于\eqref{eq:123}，\eqref{eq:134}和\eqref{eq:135}的产生湮灭算符的基本对易关系。

采用与处理离散本征谱完全一样的手段，通过产生湮灭算符将一个任意的包含单体项和两体项的观察算法$\widehat{A}$（见\eqref{eq:141}），用二次量子化形式表达：

<mj>
\begin{align}
\label{eq:214}
\begin{split}
\widehat{A}\equiv&\sum_{p,r}\langle\varphi_{\alpha_p}|\widehat{A}_1|\varphi_{\alpha_r}\rangle a_p^\dagger a_r+\\
&+\frac{1}{2}\sum_{\substack{p,r,\\s,t}}\langle\varphi_{\alpha_p}^{(1)}\varphi_{\alpha_r}^{(2)}|\widehat{A}_2|\varphi_{\alpha_t}^{(1)}\varphi_{\alpha_s}^{(2)}\rangle a_p^\dagger a_r^\dagger a_s a_t
\end{split}
\end{align}
</mj>

和连续本征谱的情况唯一的不同就是，此处的两体矩阵元必须由非对称化的两粒子态构成，而在\eqref{eq:147}中可以使用对称化（反对称化）的态矢。其原因全在于所用的归一化因子不同。

> **附注**：  
> 考虑如何用厄米算符$\hat{n}\_i=\hat{a}_i^\dagger\hat{a}\_i$表示力学量（观察算符）。
>
> 首先考虑单粒子力学量$\widehat{A}_1$：
> 
> \begin{equation}
\widehat{A}\_1\|a\_i\rangle=a\_i\|a\_i\rangle
\end{equation}
> 
> 若选取表象A，为$\widehat{A}_1$的自身表象，在按照$a_i$分布的福克空间$\|N;\cdots n_i\cdots\rangle^{(\varepsilon)}$中，其对应的体系力学量算符为
> 
> \begin{equation}
\widehat{A}\_1=\sum\_ia\_i\hat{n}\_i=\sum\_ia\_i\hat{a}\_i^\dagger\hat{a}\_i
\end{equation}
> 
> 若另选表象B，此时$\widehat{A}_{1}$无确定值，做表象变换
> 
> <mj>\begin{align}
\widehat{A}_1&=\sum_ia_i\hat{a}_i^\dagger\hat{a}_i=\sum_{ijk}a_iS_{ji}S_{ik}\hat{b}_j^\dagger\hat{b}_k=\\
&=\sum_{jk}\hat{b}_j^\dagger\hat{b}_k\sum_ia_i\langle b_j|a_i\rangle\langle a_i|b_k\rangle=\\\
&=\sum_{jk}\hat{b}_j^\dagger\hat{b}_k\sum_i\langle b_j|\widehat{A}_1|a_i\rangle\langle a_i|b_k\rangle=\\
&=\sum_{jk}\hat{b}_j^\dagger\hat{b}_k\sum_i\langle b_j|\widehat{A}_1|b_k\rangle
\end{align}</mj>
> 
> 其次考虑两粒子力学量$\widehat{A}_2$：
> \begin{equation}
\widehat{A}\_2\|a\_i\rangle\|a\_j\rangle=a\_{ij}\|a\_i\rangle\|a\_j\rangle
\end{equation}
> 
> 若选取表象A，为$\widehat{A}_2$的自身表象，由于两粒子可处于不同单粒子态或者同一态，其对应体系力学量算符为
> 
> <mj>\begin{align}
\widehat{A}_2&=\frac{1}{2}\sum_{i\ne j}a_{ij}\hat{n}_i\hat{n}_j+\frac{1}{2}\sum_ia_{ii}\hat{n}_i(\hat{n}_i-1)=\\\
&=\frac{1}{2}\sum_{ij}a_{ij}(\hat{n}_i\hat{n}_j-\hat{n}_j\delta_{ij})=\\\
&=\frac{1}{2}\sum_{ij}a_{ij}\hat{a}_i^\dagger\hat{a}_j^\dagger\hat{a}_j\hat{a}_i
\end{align}</mj>
> 
> 这里用到
> <mj>\begin{align}
\hat{n}_i\hat{n}_j-\hat{n}_j\delta_{ij}&=\hat{a}_i^\dagger\hat{a}_i\hat{a}_j^\dagger\hat{a}_j-\hat{a}_j^\dagger\hat{a}_j\delta_{ij}=\\\
&=\hat{a}_i^\dagger\left(\delta_{ij}+\varepsilon\hat{a}_j^\dagger\hat{a}_i\right)\hat{a}_j-\hat{a}_j^\dagger\hat{a}_j\delta_{ij}=\\\
&=\varepsilon\hat{a}_i^\dagger\hat{a}_j^\dagger\hat{a}_i\hat{a}_j+\underbrace{\hat{a}_i^\dagger\hat{a}_j\delta_{ij}-\hat{a}_j^\dagger\hat{a}_j\delta_{ij}}_{=0}=\\\
&=\varepsilon^2\hat{a}_i^\dagger\hat{a}_j^\dagger\hat{a}_j\hat{a}_i=\\\
&=\hat{a}_i^\dagger\hat{a}_j^\dagger\hat{a}_j\hat{a}_i
\end{align}</mj>
> 
> 若另选表象B，此时$\widehat{A}_{2}$无确定值，做表象变换
> 
> <mj>\begin{align}
 \widehat{A}_2&=\frac{1}{2}\sum_{ij}a_{ij}\hat{a}_i^\dagger\hat{a}_j^\dagger\hat{a}_j\hat{a}_i=\\\
 &=\frac{1}{2}\sum_{ijklmn}a_{ij}\hat{b}_k^\dagger\hat{b}_l^\dagger\hat{b}_m\hat{b}_nS_{ki}S_{lj}S_{jm}^\dagger S_{in}^\dagger=\\\
 &=\frac{1}{2}\sum_{ijklmn}a_{ij}\hat{b}_k^\dagger\hat{b}_l^\dagger\hat{b}_m\hat{b}_n\langle b_k|a_i\rangle\langle b_l|a_j\rangle\langle a_j|b_m\rangle\langle a_i|b_n\rangle=\\\
 &=\frac{1}{2}\sum_{klmn}\hat{b}_k^\dagger\hat{b}_l^\dagger\hat{b}_m\hat{b}_n\sum_{ij}a_{ij}\langle b_k|a_i\rangle\langle b_l|a_j\rangle\langle a_i|b_n\rangle\langle a_j|b_m\rangle=\\\
 &=\frac{1}{2}\sum_{klmn}\hat{b}_k^\dagger\hat{b}_l^\dagger\hat{b}_m\hat{b}_n\sum_{ij}a_{ij}\langle b_k|\langle b_l|a_j\rangle|a_i\rangle\langle a_i|b_n\rangle\langle a_j|b_m\rangle=\\\
 &=\frac{1}{2}\sum_{klmn}\hat{b}_k^\dagger\hat{b}_l^\dagger\hat{b}_m\hat{b}_n\sum_{ij}\langle b_k|\langle b_l|\widehat{A}_2|a_j\rangle|a_i\rangle\langle a_i|b_n\rangle\langle a_j|b_m\rangle=\\\
 &=\frac{1}{2}\sum_{klmn}\hat{b}_k^\dagger\hat{b}_l^\dagger\hat{b}_m\hat{b}_n\sum_{ij}\langle b_k|\langle b_l|\widehat{A}_2|a_j\rangle\langle a_j|b_m\rangle|b_n\rangle=\\\
 &=\frac{1}{2}\sum_{klmn}\hat{b}_k^\dagger\hat{b}_l^\dagger\hat{b}_m\hat{b}_n\sum_{ij}\langle b_k|\langle b_l|\widehat{A}_2|b_m\rangle|b_n\rangle
 \end{align}</mj>


类似于\eqref{eq:151}中的占有密度算符，在离散情况下，引入占有数算符：

\begin{equation}
\label{eq:215}
\hat{n}\_r=a\_r^\dagger a\_r
\end{equation}

从\eqref{eq:203}和\eqref{eq:207}可见，福克态是占有数算符$\hat{n}\_r$的本征矢：

\begin{equation}
\label{eq:216}
\hat{n}\_r\|N;\cdots n\_r\cdots\rangle^{(\varepsilon)}=n\_r\|N;\cdots n\_r\cdots\rangle^{(\varepsilon)}
\end{equation}

$\hat{n}\_r$回答了有多少粒子占据第$r$个单粒子态。

接着还有粒子数算符：

\begin{equation}
\label{eq:217}
\widehat{N}=\sum\_r\hat{n}\_r
\end{equation}

它的本征矢是以总粒子数为本征值的福克态：

<mj>
\begin{align}
\label{eq:218}
\begin{split}
\widehat{N}|N;\cdots n_r\cdots\rangle^{(\varepsilon)}&=\left(\sum_r n_r\right)|N;\cdots n_r\cdots\rangle^{(\varepsilon)}=\\\
&=N|N;\cdots n_r\cdots\rangle^{(\varepsilon)}
\end{split}
\end{align}
</mj>

下面几个对费米子和玻色子同样适用的对易式可以根据\eqref{eq:211}，\eqref{eq:212}和\eqref{eq:213}推导出来，这里不再赘述：

<mj>
\begin{align}
\label{eq:219}
\left[\hat{n}_r,a_p^\dagger\right]_-&=\delta_{rp}a_p^\dagger\\\
\label{eq:220}
\left[\hat{n}_r,a_p\right]_-&=-\delta_{rp}a_p\\\
\label{eq:221}
\left[\widehat{N},a_p^\dagger\right]_-&=a_p^\dagger\\\
\label{eq:222}
\left[\widehat{N},a_p\right]_-&=-a_p
\end{align}
</mj>

## 参考
1. Wolfgang Nolting *多体物理学基础：原理和方法*
2. 科恩·塔诺季 *量子力学*
3. 朗道 *量子力学*
4. 刘觉平 *量子力学*
5. 马中骐 *物理学中的群论*
