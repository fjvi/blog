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


