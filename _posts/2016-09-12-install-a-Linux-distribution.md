---
layout: post
title: How to install a Linux distribution
categories: computer
tags: Linux
---

Linux这个如雷贯耳,与 Windows,Mac OS 三足鼎立的操作系统,在很多人的心中是程序员才用的东西,但是现代绝大多数的科学计算任务,都是在 Linux 平台上进行的,比如在计算化学中,经典的 Gaussian 程序只在 Linux 上支持多线程,在计算物理中其作用更是不言而喻。

![Linux distributions](http://linuxmentors.com/wp-content/uploads/2015/10/linux_distros.png)

## 跨出认识 Linux 的第一步
认识一个东西,不必急于搞清其本质,首要的是先接触,熟悉其外貌。那么认识 Linux 的第一步就是学会安装 Linux 。

安装 Linux,安装在哪里呢?当然是硬盘里啦,但是 Linux 中对硬盘的叫法与 Windows 不同,它把装在主板上的硬盘叫做`/dev/hd`,并以 a、b、c、d 命名多个硬盘。对于在硬盘上的分区,它是这么叫的: 以`/dev/hda` 为例,假如`/dev/had` 分了 P1、P2、P3、P4 四个区(就是你的 Windows 中的CDEF...盘),那么这四个区就分别叫做 P1:`/dev/hda1`、P2:`/dev/hda5`、P3:`/dev/hda6`、P4:`/dev/hda7`。(先别管为什么没有 2、3 和 4 )

### 分盘
由于我们对 Linux 还不熟悉,就先让我们的老朋友 Windows 来和他一起工作,增进感情,然后我们再和 Linux 慢慢熟悉起来。所以现在我们想让 Linux 和 Windows 共存,也就是安装双操作系统。 Windows 先入为主,所以它继续占据来硬盘的第一个位置——C 盘,用 Linux 的话来讲,就是`/dev/hda1`(如果 Windows 是安装在`/dev/had` 硬盘上的话)。所以,Linux 就要排排后,我们从哪个分区里给 Linux 腾点位置呢?就看哪个盘空间比较足,能腾出地方来,这里还是推荐从最后一个分区中腾点空间给 Linux ,这样误操作的几率更小~

那么怎么腾点空间出来呢?其实 Windows 就可以实现,只要是 Win7 及以上的系统,就只需右键桌面上的电脑图标,在在菜单中点击管理选项,然后点击磁盘管理选项，在这个地方,右击最后一个分区,我这里是 G ,(得保证您有 10G 左右的空闲空间以容纳Linux),点击压缩卷,然后输入想腾出的空间的大小。点击完成后等待一会儿就有一个绿色的新卷被分出来。

![](https://mageluer.github.io/assets/images/how-to-install-a-linux-distribution-02.jpg)

### 安装系统
接下来我们看看到底怎么安装 Linux。想认识新朋友,总得有引荐的人嘛,这里我们采用一个最最最简单有效的方式来把 Linux 引荐给我们的电脑。首先得有一块 U 盘,其次要选择一个 Linux 的发行版,发行版有很多,但它们都使用同一个系统内核(心脏),那就是 Linux 内核!著名的发行版有 Fedora、Ubuntu、Cent OS 等等。这里我们选择Fedora~(因为作者喜欢帽子,哈哈,其实 Fedora 在安装时时最 User-Friendly 的,但也仅限于安装的时候......),可以在 Fedora 官网下载最新的版本,如果您选择 Ubuntu 或 CentOS,同样可以在它们的官网下载到系统文件。这种文件一般是 iso 文件。然后您要下载一个软件,`Universal Usb Installer`,简称 UUI,这就是我们善良的引荐者!打开它,在 Step1 中选择您下载到的系统,我选择的是 `Fedora 32/64bit`。然后在 Step2 中选择您下载的 iso 文件,然后在 Step3 中选择您的 U 盘,点击 Create,等待......等待......等待,等进度条走完就大功告成了!提醒一下您,**请提前备份 U 盘里的文件**~

然后就是正式的引荐过程。重启电脑,然后选择引导方式,额,这个引导方式就是指电脑到底选择从哪个硬件读取系统,因为我们已经把 Fedora 系统写入了 U 盘,所以这个时候 U 盘就可以引导电脑启动了。但是,不同的电脑有不同的选择引导的办法, Lenovo 是在开机时按住 `F10`,一般的电脑就是按住 `ESC` 键,这样做之后会,屏幕显示一个选择硬件的界面,这个时候只要选择你的 U 盘就行了,如果 U 盘是 `Kingston` 的,那就选`Kingston`,是别的品牌的,就选相应品牌的名称,如果界面里没有品牌名称,那一般要选`General U disk` 之类的选项,如果还是没有,那么..........................................换个插口试试吧~

选择了 U 盘引导之后,就会出现一个安装还是试用的选项(`Install` 和 `Try`),我们选`Install`,然后做最最重要的一步就是把系统安装到您之前腾出来的那个新卷里面,如果腾地方的时候用的是最后一个分区,那么新卷就在这个分区之后,也就是整个区中的最后一个区!可以选择让 Fedora 自动配置这个新卷,相信安装界面中的英文对大家而言都不在话下,之后按照提示填写一些必要的信息,等待再等待,就等着迎接 triumph 啦~

![](https://fossbytes.com/wp-content/uploads/2016/05/fedora-24-beta-download.jpg)

> 再提醒一次!**必须把 Linux 装在新分出的卷上**,不然,惨痛的后果一定会让你难忘终身!这里给出一个判断方法,如果压缩时用的是 `D` 盘,那么新卷就是`/dev/hda6`,压缩时用的是 `E` 盘,那么新卷就是`/dev/hda7`,以此类推!
{: .attention}

### Acknowledgement
> 感谢 [Mulliken](https://mulliken.github.io) 的帮助,完成文章大部分内容。
{: .thanks}
