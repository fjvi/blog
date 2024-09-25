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
$ wsl --install -d <Distribution Name>　或者　$ wsl --install　默认安装Ubuntu
```

# 查看已安装的Linux版本
```
$ wsl --list -v　或者　$ wsl -l -v
```

# 切换默认Linux版本
```
$ wsl -s <DistributionName>　或者　$ wsl --set-default <DistributionName>
```

