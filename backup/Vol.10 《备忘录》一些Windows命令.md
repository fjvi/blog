# 查看内网IP
```
ipconfig
```

# 查看公网IP
```
curl ipinfo.io
```

# 网络诊断
```
tracert www.google.com
```

# WIFI密码
```
netsh wlan show profiles                         　←查看名字
netsh wlan show profiles name=xxxx key=clear        ←名字代入
```

# 强制启动ie老版浏览器
```
CreateObject("InternetExplorer.Application").Visible=true
保存为vbs
```

# 修复系统文件
```
sfc /scannow
```

# 恢复应用商店
```
wsreset -i
```


# 删除Windows内置app [win11debloat](https://github.com/raphire/win11debloat/)
```
irm "https://win11debloat.raphi.re/" | iex
```

# 修改Win设置 [ChrisTitusTech/winutil](https://github.com/ChrisTitusTech/winutil/)
```
irm "https://christitus.com/win" | iex
```

# 切换成Win10的右键菜单
```
reg add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve
````

# 恢复成Win11的右键菜单
```
reg delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}" /f 
```

# 永久暂停Windows自动更新
```
reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsUpdate\UX\Settings" /v FlightSettingsMaxPauseDays /t reg_dword /d 9999 /f
```

# Windows家庭版开启hyper-v
```
pushd "%~dp0"
dir /b %SystemRoot%servicingPackages*Hyper-V*.mum >hv.txt
for /f %%i in ('findstr /i . hv.txt 2^>nul') do dism /online /norestart /add-package:"%SystemRoot%servicingPackages%%i"
del hv.txt
Dism /online /enable-feature /featurename:Microsoft-Hyper-V -All /LimitAccess /ALL
pause
```

`Gmeek-html<img src="https://gitee.com/tech-shrimp/me/raw/master/doc/images/240119/3.png">`

将文本文档改名为"xxx.bat"，需注意.bat是扩展名
完成后重启电脑

# Windows特殊文件夹
- System.Environmentを使って特殊フォルダ一覧リストを出力
```
[Environment+SpecialFolder]::GetNames([Environment+SpecialFolder]) | Sort-Object

↓↓特殊フォルダの一覧
AdminTools
ApplicationData
CDBurning
CommonAdminTools
CommonApplicationData
CommonDesktopDirectory
CommonDocuments
CommonMusic
CommonOemLinks
CommonPictures
CommonProgramFiles
CommonProgramFilesX86
CommonPrograms
CommonStartMenu
CommonStartup
CommonTemplates
CommonVideos
Cookies
Desktop
DesktopDirectory
Favorites
Fonts
History
InternetCache
LocalApplicationData
LocalizedResources
MyComputer
MyDocuments
MyMusic
MyPictures
MyVideos
NetworkShortcuts
Personal
PrinterShortcuts
ProgramFiles
ProgramFilesX86
Programs
Recent
Resources
SendTo
StartMenu
Startup
System
SystemX86
Templates
UserProfile
Windows
```

- 各特殊フォルダのパスの取得方法は、Enviroment.GetFolderPath() メソッドを使用
```
[Environment]::GetFolderPath("Desktop")
> C:\Users\xyz\Desktop

[Environment]::GetFolderPath("AdminTools")
> C:\Users\xyz\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Administrative Tools

[Environment]::GetFolderPath("ProgramFiles")
> C:\Program Files (x86)
```


- 特殊フォルダのパス一覧を出力
```
$SpecialFolders = @{}
$names = [Environment+SpecialFolder]::GetNames([Environment+SpecialFolder]) | Sort-Object
$names | Format-Table

foreach($name in $names)
{
  if($path = [Environment]::GetFolderPath($name)){
    $SpecialFolders[$name] = $path
  }
}
$SpecialFolders | Format-Table

# ↓↓パス一覧
Name                           Value
----                           -----
System                         C:\WINDOWS\system32
CommonApplicationData          C:\ProgramData
CommonVideos                   C:\Users\Public\Videos
CDBurning                      C:\Users\win11\AppData\Local\Microsoft\Windows\Burn\Burn
MyVideos                       C:\Users\win11\Videos
ProgramFilesX86                C:\Program Files (x86)
AdminTools                     C:\Users\win11\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Administrative Tools
History                        C:\Users\win11\AppData\Local\Microsoft\Windows\History
CommonDocuments                C:\Users\Public\Documents
Templates                      C:\Users\win11\AppData\Roaming\Microsoft\Windows\Templates
CommonDesktopDirectory         C:\Users\Public\Desktop
UserProfile                    C:\Users\win11
Startup                        C:\Users\win11\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup
InternetCache                  C:\Users\win11\AppData\Local\Microsoft\Windows\INetCache
SystemX86                      C:\WINDOWS\SysWOW64
CommonStartMenu                C:\ProgramData\Microsoft\Windows\Start Menu
MyPictures                     C:\Users\win11\Pictures
Recent                         C:\Users\win11\AppData\Roaming\Microsoft\Windows\Recent
Fonts                          C:\WINDOWS\Fonts
SendTo                         C:\Users\win11\AppData\Roaming\Microsoft\Windows\SendTo
CommonProgramFiles             C:\Program Files\Common Files
ProgramFiles                   C:\Program Files
Favorites                      C:\Users\win11\Favorites
CommonStartup                  C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Startup
Windows                        C:\WINDOWS
DesktopDirectory               C:\Users\win11\Desktop
LocalizedResources             C:\WINDOWS
MyMusic                        C:\Users\win11\Music
ApplicationData                C:\Users\win11\AppData\Roaming
CommonPictures                 C:\Users\Public\Pictures
CommonPrograms                 C:\ProgramData\Microsoft\Windows\Start Menu\Programs
Desktop                        C:\Users\win11\Desktop
PrinterShortcuts               C:\Users\win11\AppData\Roaming\Microsoft\Windows\Printer Shortcuts
CommonAdminTools               C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Administrative Tools
NetworkShortcuts               C:\Users\win11\AppData\Roaming\Microsoft\Windows\Network Shortcuts
CommonMusic                    C:\Users\Public\Music
CommonProgramFilesX86          C:\Program Files (x86)\Common Files
Programs                       C:\Users\win11\AppData\Roaming\Microsoft\Windows\Start Menu\Programs
Resources                      C:\WINDOWS\resources
MyComputer                     C:\WINDOWS
CommonTemplates                C:\ProgramData\Microsoft\Windows\Templates
CommonOemLinks                 C:\WINDOWS
MyDocuments                    C:\Users\win11\Documents
StartMenu                      C:\Users\win11\AppData\Roaming\Microsoft\Windows\Start Menu
Cookies                        C:\Users\win11\AppData\Local\Microsoft\Windows\INetCookies
LocalApplicationData           C:\Users\win11\AppData\Local
Personal                       C:\Users\win11\Documents
```
