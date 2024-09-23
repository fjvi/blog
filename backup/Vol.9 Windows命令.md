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

# 强制启动ie浏览器
```
CreateObject("InternetExplorer.Application").Visible=true
保存为vbs
```

# 修复系统文件
```
sfc /scannow
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
