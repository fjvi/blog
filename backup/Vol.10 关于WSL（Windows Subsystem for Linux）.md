# 关于 Linux 的 Windows 子系统 (WSL) 
Windows 的一项功能，可用于在 Windows 计算机上运行 Linux 环境，而无需单独的虚拟机或双引导。 WSL 旨在为希望同时使用 Windows 和 Linux 的开发人员提供无缝高效的体验。

# 前提条件
开启以下2个功能 （系统 > 附加功能 > 其他功能 ） 
- WSL（Windows Subsystem for Linux）
- 虚拟机平台


# WSL命令
> https://learn.microsoft.com/ja-jp/windows/wsl/basic-commands


# WSL 的版本
```
wsl --version
```

# WSL 的状態
```
wsl --status
```

# 帮助
```
wsl --help
```

# 查看可安装的Linux版本

```
$ wsl --list --online　或者　$ wsl -l -o
```

|NAME|FRIENDLY NAME|Default|
|---|---|---|
|Ubuntu                        |Ubuntu |★|
|Debian                         |Debian GNU/Linux||
|kali-linux                      |Kali Linux Rolling||
|Ubuntu-18.04              |Ubuntu 18.04 LTS||
|Ubuntu-20.04              |Ubuntu 20.04 LTS||
|Ubuntu-22.04              |Ubuntu 22.04 LTS||
|Ubuntu-24.04              |Ubuntu 24.04 LTS||
|OracleLinux_7_9           |Oracle Linux 7.9||
|OracleLinux_8_7           |Oracle Linux 8.7||
|OracleLinux_9_1           |Oracle Linux 9.1||
|openSUSE-Leap-15.6   |openSUSE Leap 15.6||
|SUSE-Linux-Enterprise-15-SP5   |SUSE Linux Enterprise 15 SP5||
|SUSE-Linux-Enterprise-15-SP6   |SUSE Linux Enterprise 15 SP6||
|openSUSE-Tumbleweed             |openSUSE Tumbleweed||


# 安装 WSL
```
$ wsl --install -d <Distribution Name>　或者　$ wsl --install　**默认安装Ubuntu**
```

# 查看已安装的Linux版本
```
$ wsl --list --verbose　或者　$ wsl -l -v
```





# 全部关闭
```
wsl --shutdown
```

# 关闭指定Linux版本
```
wsl --terminate <Distribution Name>
```

# 查看IP
- WSL 2 経由でインストールされた Linux ディストリビューションの IP アドレスを返します (WSL 2 VM アドレス)
```
wsl hostname -I
```
- WSL 2 から見た Windows マシンの IP アドレスを返します (WSL 2 VM)
```
ip route show | grep -i default | awk '{ print $3}'
```





# 切换默认Linux版本
```
$ wsl -s <DistributionName>　或者　$ wsl --set-default <Distribution Name>
```

# 快速启动默认Linux版本
```
$ wsl ~
```

# 启动指定Linux版本
```
$ wsl -d <DistributionName>
```

# 卸载Linux
```
$ wsl --unregister <DistributionName>
```

# 备份Linux
```
$ wsl --export <Distribution Name> xxx.tar
```

# 导入Linux
```
$ wsl --import <Distribution Name> <Install-Location> xxx.tar
```

# マウント
```
wsl --mount <DiskPath>
```

# マウント解除
```
wsl --unmount <DiskPath>
```