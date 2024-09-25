`Gmeek-html<img src="https://erainnovator.com/wp-content/uploads/2021/04/PowerShell.png">`

## 获取 PowerShell Command一覧

```
$ gcm　或者   $ get-command
```

## 获取 PowerShell Alias一覧

```
$ gal　或者   $ Get-Alias
```

`Gmeek-html<img src="https://linuxhint.com/wp-content/uploads/2022/01/create-powershell-alias-01.png">`

## PowerShell Alias一覧

|PowerShell Alias|PowerShell Command|例子|
|---|---|---|
|gcm|  Get-Command|例：`Get-Command Get-*`　查找所有以 Get- 开头的 cmdlets|
|gal|  Get-Alias|显示PowerShell Alias一覧|
|`pwd`🔥|  Get-Location|显示当前所在目录|
|gl|  Get-Location|同上|
|`ls`🔥|  Get-ChildItem|例：`Get-ChildItem -Path .`　 列出当前目录下的所有文件和目录|
|`dir`🔥|  Get-ChildItem|同上|
|gci|  Get-ChildItem|同上|
|`cd`🔥|   Set-Location|例：`Set-Location C:\Users\YourName\Documents`  切换到用户的文档目录|
|chdir|Set-Location|同上|
|sl|  Set-Location|同上|
|`copy`🔥|  Copy-Item|例：`Copy-Item C:\source\test.txt C:\destination\`  复制文件 test.txt 到另一个目录|
|`cp`🔥|  Copy-Item|同上|
|cpi|  Copy-Item|同上|
|`mv`🔥| Move-Item|例：`Move-Item C:\temp\oldname.txt C:\temp\newfolder\newname.txt`  将文件 oldname.txt 移动到 newfolder 并重命名为 newname.txt|
|move|  Move-Item|同上|
|mi|  Move-Item|同上|
|`ren`🔥|  Rename-Item|例：`Rename-Item C:\temp\oldname.txt C:\temp\newname.txt`  将文件 oldname.txt 重命名为 newname.txt|
|rni|  Rename-Item|同上|
|`md`🔥|  mkdir|
|`del`🔥|  Remove-Item|例：`Remove-Item C:\temp\test.txt -Force`  删除名为 test.txt 的文件|
|`rm`🔥|  Remove-Item|同上|
|`rmdir`🔥|  Remove-Item|同上|
|erase|  Remove-Item|同上|
|rd|  Remove-Item|同上|
|ri|  Remove-Item|同上|
|`cat`🔥|  Get-Content|例：`$content = Get-Content -Path "C:\temp\input.txt"`  读取文件内容|
|`type`🔥|  Get-Content|同上|
|`diff`🔥|  Compare-Object|例：`$list1 = 1..5 $list2 = 2..6 Compare-Object -ReferenceObject $list1 -DifferenceObject $list2`  比较两个数字列表的不同之处|
|`compare`🔥|  Compare-Object|同上|
|`ps`🔥|  Get-Process|获取所有运行中的进程|
|gps|  Get-Process|同上|
|`start`🔥|  Start-Process|例：`Start-Process notepad`  启动记事本应用程序|
|`saps`✨️|  Start-Process|同上|
|`kill`🔥|  Stop-Process|例：`Stop-Process -Name notepad`  终止所有名为 notepad 的进程|
|`spps`✨️|  Stop-Process|同上|
|`gsv`🔥|  Get-Service|获取所有服务的状态|
|`sasv`✨️|  Start-Service|例：`Start-Service -Name spooler`  启动 Print Spooler 服务|
|`spsv`✨️|  Stop-Service|例：`Stop-Service -Name spooler`  停止 Print Spooler 服务|
|`rssv`✨️|  Restart-Service|例：`Restart-Service -Name spooler`  重启 Print Spooler 服务|
|`wget`🔥|  Invoke-WebRequest|例：`Invoke-WebRequest -Uri "https://api.github.com/repos/powershell/powershell/releases/latest"`  获取 GitHub 上最新发布的版本信息|
|`curl`🔥|  Invoke-WebRequest|同上|
|iwr|  Invoke-WebRequest|同上|
|`write`🔥|  Write-Host|例：`Write-Host "Hello, world!"`  输出 Hello, world!|
|`echo`🔥|  Write-Output|例：`Write-Output "Hello, world!"`  输出 Hello, world!|
|`clear`🔥|Clear-Host|清除控制台屏幕|
|`cls`🔥|  Clear-Host|同上|
|`man`🔥|  help|例：`Get-Help Get-Process`  获取 Get-Process 的帮助文档|
|ise|  powershell_ise.exe|
|%|    ForEach-Object|
|?|    Where-Object|例：`Get-Process \ Where-Object { $_.CPU -gt 10 }`  获取 CPU 占用率大于 10% 的所有进程|
|where|  Where-Object|同上|
|ac|   Add-Content|
|asnp| Add-PSSnapin|
|CFS|  ConvertFrom-String|
|clc|  Clear-Content|
|clhy| Clear-History|
|cli|  Clear-Item|
|clp|  Clear-ItemProperty|
|clv|  Clear-Variable|
|cnsn| Connect-PSSession|
|cpp|  Copy-ItemProperty|
|cvpa|  Convert-Path|
|dbp|  Disable-PSBreakpoint|
|dnsn|  Disconnect-PSSession|
|ebp|  Enable-PSBreakpoint|
|ipal|  Import-Alias|
|epal|  Export-Alias|
|ipcsv|  Import-Csv|例：`$data = Import-Csv -Path "C:\temp\data.csv"`  从 CSV 文件导入数据|
|epcsv|  Export-Csv|例：`$data \ Export-Csv -Path "C:\temp\output.csv" -NoTypeInformatio`  将数据导出为 CSV 文件|
|epsn|  Export-PSSession|
|etsn|  Enter-PSSession|
|exsn|  Exit-PSSession|
|fc|  Format-Custom|
|fhx|  Format-Hex|
|fl|  Format-List|
|foreach|  ForEach-Object|
|ft|  Format-Table|
|fw|  Format-Wide|
|`gbp`🌛|  Get-PSBreakpoint|
|sc|  Set-Content|例：`"Hello, world!" \ Set-Content -Path "C:\temp\output.txt"`  写入文件内容|
|`gc`🌛|  Get-Content|例：`$content = Get-Content -Path "C:\temp\input.txt"`  读取文件内容|
|`gcb`🌛|  Get-Clipboard|
|`gcs`🌛|  Get-PSCallStack|
|`gdr`🌛|  Get-PSDrive|
|`gi`🌛|  Get-Item|
|`gin`🌛|  Get-ComputerInfo|
|`gjb`🌛|  Get-Job|
|`gm`🌛|  Get-Member|
|`gmo`🌛|  Get-Module|
|`gp`🌛|  Get-ItemProperty|
|`gpv`🌛|  Get-ItemPropertyValue|
|`gsn`🌛|  Get-PSSession|
|`gsnp`🌛|  Get-PSSnapin|
|`gtz`🌛|  Get-TimeZone|
|`gu`🌛|  Get-Unique|
|`gv`🌛|  Get-Variable|
|`gwmi`🌛|  Get-WmiObject|例：`Get-WmiObject -Class Win32_OperatingSystem`  获取操作系统信息|
|`ghy`🌛|  Get-History|
|`h`🌛|  Get-History|
|`history`🌛|  Get-History|
|group|  Group-Object|例：`Get-Process \Group-Object -Property MainModule.FileName`  按主模块的文件名分组进程|
|icm|  Invoke-Command|
|iex|  Invoke-Expression|
|ihy|  Invoke-History|
|ii|  Invoke-Item|
|ipmo|  Import-Module|
|ipsn|  Import-PSSession|
|irm|  Invoke-RestMethod|
|iwmi|  Invoke-WmiMethod|
|lp|  Out-Printer|
|measure|  Measure-Object|
|mount|  New-PSDrive|
|mp|  Move-ItemProperty|
|nal|  New-Alias|
|ndr|  New-PSDrive|
|ni|  New-Item|例：`New-Item -ItemType Directory -Path .\myFolder`  在当前目录下创建一个名为 myFolder 的新目录|
|nmo|  New-Module|
|npssc|  New-PSSessionConfigur|
|nsn|  New-PSSession|
|nv|  New-Variable|
|ogv|  Out-GridView|
|oh|  Out-Host|
|popd|  Pop-Location|
|pushd|  Push-Location|
|r|  Invoke-History|
|rbp|  Remove-PSBreakpoint|
|rcjb|  Receive-Job|
|rcsn|  Receive-PSSession|
|rdr|  Remove-PSDrive|
|rjb|  Remove-Job|
|rmo|  Remove-Module|
|rnp|  Rename-ItemProperty|
|rp|  Remove-ItemProperty|
|rsn|  Remove-PSSession|
|rsnp|  Remove-PSSnapin|
|rujb|  Resume-Job|
|rv|  Remove-Variable|
|rvpa|  Resolve-Path|
|rwmi|  Remove-WmiObject|
|sal|  Set-Alias|
|sbp|  Set-PSBreakpoint|
|scb|  Set-Clipboard|
|select|  Select-Object|
|set|  Set-Variable|
|shcm|  Show-Command|
|si|  Set-Item|
|sleep|  Start-Sleep|
|sls|  Select-String|例：`Select-String -Path "C:\temp\log.txt" -Pattern "error"`  在日志文件中搜索含有 "error" 的行|
|sort|  Sort-Object|例：`Get-Process \ Sort-Object -Property CPU -Descending`   按 CPU 占用率降序排列所有进程|
|sp|  Set-ItemProperty|
|`sajb`✨️|  Start-Job|
|`spjb`✨️|  Stop-Job|
|stz|  Set-TimeZone|
|sujb|  Suspend-Job|
|sv|  Set-Variable|
|swmi|  Set-WmiInstance|在 WMI 中创建或修改实例|
|tee|  Tee-Object|
|trcm|  Trace-Command|
|wjb|  Wait-Job|






## 常用PowerShell命令
　　1. 像文件系统那样操作Windows Registry——cd hkcu:
　　2. 在文件里递回地搜索某个字符串——dir –r | select string "searchforthis" 
　　3. 使用内存找到五个进程——ps | sort –p ws | select –last 5
　　4. 循环（停止，然后重启）一个服务，如DHCP——Restart-Service DHCP
　　5. 在文件夹里列出所有条目——Get-ChildItem – Force
　　6. 递归一系列的目录或文件夹——Get-ChildItem –Force c:\directory –Recurse
　　7. 在目录里移除所有文件而不需要单个移除——Remove-Item C:\tobedeleted –Recurse
　　8. 重启当前计算机——(Get-WmiObject -Class Win32_OperatingSystem -ComputerName .).Win32Shutdown(2)
　　9. 获取计算机组成或模型信息——Get-WmiObject -Class Win32_ComputerSystem
　　10. 获取当前计算机的BIOS信息——Get-WmiObject -Class Win32_BIOS -ComputerName .
　　11. 列出所安装的修复程序（如QFE或Windows Update文件）——Get-WmiObject -Class Win32_QuickFixEngineering -ComputerName .
　　12. 获取当前登录计算机的用户的用户名—— Get-WmiObject -Class Win32_ComputerSystem -Property UserName -ComputerName .
　　13. 获取当前计算机所安装的应用的名字——Get-WmiObject -Class Win32_Product -ComputerName . | Format-Wide -Column 1
　　14. 获取分配给当前计算机的IP地址——Get-WmiObject -Class Win32_NetworkAdapterConfiguration -Filter IPEnabled=TRUE -ComputerName . | Format-Table -Property IPAddress
　　15. 获取当前机器详细的IP配置报道——Get-WmiObject -Class Win32_NetworkAdapterConfiguration -Filter IPEnabled=TRUE -ComputerName . | Select-Object -Property [a-z]* -ExcludeProperty IPX*,WINS*
　　16. 找到当前计算机上使用DHCP启用的网络卡——Get-WmiObject -Class Win32_NetworkAdapterConfiguration -Filter "DHCPEnabled=true" -ComputerName .
　　17. 在当前计算机上的所有网络适配器上启用DHCP——Get-WmiObject -Class Win32_NetworkAdapterConfiguration -Filter IPEnabled=true -ComputerName . | ForEach-Object -Process {$_.EnableDHCP()}
　　18. 在远程计算机上安装MSI包——(Get-WMIObject -ComputerName TARGETMACHINE -List | Where-Object -FilterScript {$_.Name -eq "Win32_Product"}).Install(\MACHINEWHEREMSIRESIDES\path\package.msi)
　　19. 使用基于MSI的应用升级包升级所安装的应用——(Get-WmiObject -Class Win32_Product -ComputerName . -Filter "Name='name_of_app_to_be_upgraded'").Upgrade(\MACHINEWHEREMSIRESIDES\path\upgrade_package.msi)
　　20. 从当前计算机移除MSI包——(Get-WmiObject -Class Win32_Product -Filter "Name='product_to_remove'" -ComputerName . ).Uninstall()
　　21. 一分钟后远程关闭另一台机器——Start-Sleep 60; Restart-Computer –Force –ComputerName TARGETMACHINE
　　22. 添加打印机——(New-Object -ComObject WScript.Network).AddWindowsPrinterConnection(\printerserver\hplaser3)
　　23. 移除打印机——(New-Object -ComObject WScript.Network).RemovePrinterConnection("\printerserver\hplaser3 ")
　　24. 进入PowerShell会话——invoke-command -computername machine1, machine2 -filepath c:\Script\script.ps1