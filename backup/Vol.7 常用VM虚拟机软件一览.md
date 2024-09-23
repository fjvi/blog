# 常用虚拟机软件一览
虚拟机的使用场景很多，如搭建测试环境、在Windows系统中安装Linux或在Mac机器上运行Windows系统、甚至还可以用来进行安全实验。虚拟机的关键优势在于实现了跟原生系统的完全隔离，这使得我们可以在虚拟机上做各类测试。本文将介绍目前市面上适合个人用户使用的9款虚拟化软件。


- VMware家族
  - VMware Worstation Pro
  - VMware Workstation Player
  - VMware Fusion
- VirtualBox
- Microsoft Hyper-V
- KVM
- Parallels Desktop
- QEMU
- Citrix Hypervisor
- Xen
- Multipass


## 🧮 VMware家族 🔥 

### VMware Worstation Pro
VMware Workstation Pro 是行业标准桌面 Hypervisor，使用它可在 Windows 或 Linux 桌面上运行 Windows、Linux 和 BSD 虚拟机。

### VMware Workstation Player
对于大多数个人用户来说，免费版的 VMware Workstation Player 其实已经足够了。此外它体积小巧，性能好，支持3D加速，运行流畅稳定。可以说是值得推荐的首选虚拟机软件。

### VMware Fusion
VMWare Fusion 13 Pro 是 macOS 优秀的虚拟机软件「同类软件 Parallels Desktop」，兼容 macOS Ventura 和苹果 M 系列芯片，可以直接在 Mac 下运行 Windows 11、Linux 等系统。


## 🧮 VirtualBox 🔥 
VirtualBox 是一个用于 x86 硬件的通用全虚拟器，面向服务器、桌面和嵌入式应用，相对 VMware 来说 ，VirtualBox 是轻量级的虚拟软件, 最关键的是 VirtualBox 是开源免费的。


## 🧮 Microsoft Hyper-V 🔥 
嵌入在Windows的虚拟机软件。Hyper-V 让你可以在 Windows 上以虚拟机形式运行多个操作系统。


## 🧮 Parallels Desktop
Parallels Desktop是由Parallels推出的一款为苹果电脑提供硬件虚拟化的软件，产品于2006年6月发布，它是第一款能在苹果-英特尔架构的苹果电脑上使用的虚拟化软件。如果你想在Mac上运行Windows系统，那么Parallels Desktop 会是你的最佳选择。它可以在Intel 或 Apple M 系列 Mac 计算机上无缝运行 Windows 应用，最大限度地解决了 MacOS 与 Windows 软件生态差距方面的问题。


## 🧮 KVM
KVM是Kernel-based Virtual Machine的简称，是一个开源的系统虚拟化模块，自Linux 2.6.20之后集成在Linux的各个主要发行版本中，它使用Linux自身的调度器进行管理，所以相对于Xen，其核心源码很少，相对VMWare的管理方式来说是比较麻烦，但从性能上并不比VMWare差。


## 🧮 Xen
XEN最初是剑桥大学Xensource的一个开源研究项目，2003年9月发布了首个版本Xen 1.0，2007年Xensource被Citrix公司收购，开源Xen转由http://www.xen.org继续推进，该组织成员包括个人和公司（如Citrix、Oracle等）。2014年03月11日，Xen发布4.4版本，更好地支持ARM架构。Xen是运行在裸机上的虚拟化管理程序（HyperVisor），是半虚拟化（Para-Virtualization）技术的典型代表。


## 🧮 Citrix Hypervisor
Citrix Hypervisor 支持任意规模或类型的组织整合计算资源，以及将计算资源转换为虚拟工作负载，从而满足现今数据中心的要求。同时可以确保将工作负载无缝移动到云中。


## 🧮 QEMU
QEMU是一款由法布里斯·贝拉等人编写，可执行硬件虚拟化的（hardware virtualization）开源仿真器（Emulator）。QEMU与其他VM 解决方案不同的地方在于，它既是虚拟机，也是机器模拟器。QEMU可以通过动态的二进制转换，模拟CPU，并且提供一组设备模型，使它能够运行多种未修改的客户机OS。QEMU还可以通过与KVM一起使用，从而以接近真实电脑的速度来运行虚拟机。


## 🧮 Multipass
Multipass 是一个轻量虚拟机管理器，是由 Ubuntu 运营公司 Canonical 所推出的开源项目。运行环境支持 Linux、Windows、macOS。在不同的操作系统上，使用的是不同的虚拟化技术。在 Linux 上使用的是 KVM、Window 上使用 Hyper-V、macOS 中使用 HyperKit 以最小开销运行VM，支持在笔记本模拟小型云。同时，Multipass 提供了一个命令行界面来启动和管理 Linux 实例。下载一个全新的镜像需要几秒钟的时间，并且在几分钟内就可以启动并运行 VM。
