# 常用虚拟机软件一览
虚拟机的使用场景很多，如搭建测试环境、在Windows系统中安装Linux或在Mac机器上运行Windows系统、甚至还可以用来进行安全实验。虚拟机的关键优势在于实现了跟原生系统的完全隔离，这使得我们可以在虚拟机上做各类测试。本文将介绍目前市面上适合个人用户使用的9款虚拟化软件。


- VMware家族🔥
  - VMware Worstation Pro
  - VMware Workstation Player
  - VMware Fusion
- VirtualBox🔥
- Microsoft Hyper-V🔥
- Parallels Desktop
- KVM
- Xen
- Citrix Hypervisor
- QEMU
- Multipass

<br>



# 比较
|软件|操作系统|费用|稳定性|性能|推荐指数|
|---|---|---|---|---|---|
|VMware Workstation🔥|Windows、Linux|免费|中|中|★★★★|
|VMware Fusion|MacOS|有料|||
|VirtualBox🔥|Windows、Linux、MacOS|免费&开源|低|低|★★★|
|Microsoft Hyper-V🔥|Windows|免费|高|高|★★★★★|
|Parallels Desktop|MacOS|有料|||
|KVM|Linux|免费&开源|||
|Xen|Windows、Linux|免费&开源|||

<br>



## 🧮 VMware家族🔥
> 官网：https://www.vmware.com/products/desktop-hypervisor/workstation-and-fusion

`Gmeek-html<img src="https://techvccloud.mediacdn.vn/2018/11/27/vmware-15433146204021816551093-crop-15433146245501198372620.jpg">`

### VMware Worstation Pro
VMware Workstation Pro 是行业标准桌面 Hypervisor，使用它可在 Windows 或 Linux 桌面上运行 Windows、Linux 和 BSD 虚拟机。

### VMware Workstation Player
对于大多数个人用户来说，免费版的 VMware Workstation Player 其实已经足够了。此外它体积小巧，性能好，支持3D加速，运行流畅稳定。可以说是值得推荐的首选虚拟机软件。

### VMware Fusion
VMWare Fusion 13 Pro 是 macOS 优秀的虚拟机软件「同类软件 Parallels Desktop」，兼容 macOS Ventura 和苹果 M 系列芯片，可以直接在 Mac 下运行 Windows 11、Linux 等系统。

<br>



## 🧮 VirtualBox🔥
> 官网：https://www.virtualbox.org

`Gmeek-html<img src="https://upload.wikimedia.org/wikipedia/commons/d/d5/Virtualbox_logo.png">`

VirtualBox是一款免费开源的虚拟化软件，由Oracle公司开发。VirtualBox 是一个用于 x86 硬件的通用全虚拟器，面向服务器、桌面和嵌入式应用，相对 VMware 来说 ，VirtualBox 是轻量级的虚拟软件。它可以在同一台电脑上运行多个操作系统，使用户可以在不同的操作系统之间切换，并且创建不同的虚拟机。它支持Windows、Linux、MacOS和Solaris等多种操作系统，并提供多种虚拟化技术，如桥接、NAT和Host-Only等。VirtualBox是一款功能强大的虚拟化软件，被广泛应用于开发、测试、学习等领域。 

<br>



## 🧮 Microsoft Hyper-V🔥
> 官网：https://learn.microsoft.com/zh-cn/virtualization

`Gmeek-html<img src="https://www.netzen.co.uk/wp-content/uploads/2017/09/Microsoft-Hyper-V-Windows10.png">`

Microsoft Hyper-V是一款虚拟化软件，内置于Windows Server 2008及其以后的服务器操作系统中。它可以在同一台物理服务器上运行多个虚拟机，支持Windows和Linux等多种操作系统，并提供多种虚拟化技术，如动态内存、动态磁盘等。Microsoft Hyper-V还具有卓越的可靠性、性能和安全性，并且具有高度的适应性，可以在各种企业环境中广泛应用。

<br>



## 🧮 Parallels Desktop
> 官网：https://www.parallels.com/products/desktop

Parallels Desktop是由Parallels推出的一款为苹果电脑提供硬件虚拟化的软件，产品于2006年6月发布，它是第一款能在苹果-英特尔架构的苹果电脑上使用的虚拟化软件。如果你想在Mac上运行Windows系统，那么Parallels Desktop 会是你的最佳选择。它可以在Intel 或 Apple M 系列 Mac 计算机上无缝运行 Windows 应用，最大限度地解决了 MacOS 与 Windows 软件生态差距方面的问题。

<br>



## 🧮 KVM
> 官网：https://www.linux-kvm.org/page/Main_Page

KVM是Kernel-based Virtual Machine的简称，是一个开源的系统虚拟化模块，自Linux 2.6.20之后集成在Linux的各个主要发行版本中，它使用Linux自身的调度器进行管理，所以相对于Xen，其核心源码很少，相对VMWare的管理方式来说是比较麻烦，但从性能上并不比VMWare差。KVM（Kernel-based Virtual Machine）是一种基于Linux内核的虚拟化软件，可以在同一台物理服务器上运行多个虚拟机。KVM使用硬件辅助虚拟化技术，将不同的操作系统和应用程序隔离开来，提高了安全性和可靠性，并可以提高系统资源的利用率和效率。KVM具有高性能、高可靠性等优点，是一款广泛应用于企业级应用和云计算领域的虚拟化软件。

<br>



## 🧮 Xen
> 官网：https://xenproject.org

XEN最初是剑桥大学Xensource的一个开源虚拟化项目，2003年9月发布了首个版本Xen 1.0，2007年Xensource被Citrix公司收购，2014年03月11日，Xen发布4.4版本，更好地支持ARM架构。Xen是运行在裸机上的虚拟化管理程序（HyperVisor），是半虚拟化（Para-Virtualization）技术的典型代表。主要运行在Linux等多种操作系统上，它可以在同一台物理服务器上运行多个虚拟机，并使用虚拟化技术将不同的操作系统隔离开来。Xen具有高性能、高可靠性、高安全性等特点，并支持多种虚拟化技术，如硬件辅助虚拟化、半虚拟化等。Xen还支持动态配置和迁移，可以在不停机的情况下调整虚拟机的资源和配置，提高了用户的便利性和灵活性。

<br>




## 🧮 Citrix Hypervisor
> 官网：https://www.citrix.com/downloads/citrix-hypervisor

Citrix Hypervisor 支持任意规模或类型的组织整合计算资源，以及将计算资源转换为虚拟工作负载，从而满足现今数据中心的要求。同时可以确保将工作负载无缝移动到云中。

<br>



## 🧮 QEMU
> 官网：https://www.qemu.org/

QEMU是一款由法布里斯·贝拉等人编写，可执行硬件虚拟化的（hardware virtualization）开源仿真器（Emulator）。QEMU与其他VM 解决方案不同的地方在于，它既是虚拟机，也是机器模拟器。QEMU可以通过动态的二进制转换，模拟CPU，并且提供一组设备模型，使它能够运行多种未修改的客户机OS。QEMU还可以通过与KVM一起使用，从而以接近真实电脑的速度来运行虚拟机。

<br>



## 🧮 Multipass
> 官网：https://multipass.run/

Multipass 是一个轻量虚拟机管理器，是由 Ubuntu 运营公司 Canonical 所推出的开源项目。运行环境支持 Linux、Windows、macOS。在不同的操作系统上，使用的是不同的虚拟化技术。在 Linux 上使用的是 KVM、Window 上使用 Hyper-V、macOS 中使用 HyperKit 以最小开销运行VM，支持在笔记本模拟小型云。同时，Multipass 提供了一个命令行界面来启动和管理 Linux 实例。下载一个全新的镜像需要几秒钟的时间，并且在几分钟内就可以启动并运行 VM。
