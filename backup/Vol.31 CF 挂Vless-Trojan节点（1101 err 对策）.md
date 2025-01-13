# 新建Worker
创建一个worker（worker名字任意，如 cf996），替换默认的脚本 work.js 后，按部署
CF会自动生成网址   如：https://cf996.hst1189.workers.dev


# 脚本地址
为了防止1101 err, 建议使用以下混淆代码
https://github.com/yonggekkk/Cloudflare_vless_trojan
✓[Vless_workers_pages](https://github.com/yonggekkk/Cloudflare_vless_trojan/tree/main/Vless_workers_pages)
✓[Trojan_workers_pages](https://github.com/yonggekkk/Cloudflare_vless_trojan/tree/main/Trojan_workers_pages)

# 添加变量
### 1. Vless节点的变量设置
```
建议修改） uuid ⇒ 8cda8d90-9c66-4f59-8f98-d433d6238a8c
默认即可）proxyip ⇒ 默认443端口：ipv4地址、ipv6地址、域名（非443端口：ipv4地址/ipv6地址/域名：端口）
默认即可）ip1 ~ ip13 ⇒ 订阅节点：优选IP
默认即可）pt1 ~ pt13 ⇒ 订阅节点：优选IP对应端口
```

> [!TIP]
> uuid 获取方式
```
cmd ⇒ Powershell -NoExit -Command "[guid]::NewGuid()
```

### 2. Trojan节点的变量设置
```
建议修改）pswd ⇒ 万人骑密码：trojan
默认即可）proxyip ⇒ 默认443端口：ipv4地址、ipv6地址、域名（非443端口：ipv4地址/ipv6地址/域名：端口）
默认即可）ip1 ~ ip13 ⇒ 订阅节点：优选IP
默认即可）pt1 ~ pt13 ⇒ 订阅节点：优选IP对应端口
```


# 获取链接地址
上述变量设置以后，按部署，再次生成网址
打开网址，点击复制里面的链接，黏贴到软件里
https://cf996.hst1189.workers.dev/8cda8d90-9c66-4f59-8f98-d433d6238a8c



# 常用软件
1、安卓Android：[v2rayNG](https://github.com/2dust/v2rayNG/tags)、[Nekobox](https://github.com/starifly/NekoBoxForAndroid/releases)、[Karing](https://github.com/KaringX/karing/tags)、v2box

2、电脑Windows：[v2rayN](https://github.com/2dust/v2rayN/tags)、[Hiddify](https://github.com/hiddify/hiddify-next/tags)、[Karing](https://github.com/KaringX/karing/tags)

3、苹果Ios：Karing、Hiddify Proxy & VPN、Shadowrocket(小火箭)、Streisand、v2box

4、软路由Openwrt：[homeproxy](https://github.com/kiddin9/openwrt-packages)，建议使用系统自带的软件库查找更新

注意：其他平台客户端未开启分片功能情况下，workers域的6个443系TLS节点是不可用的

注意：Shadowrocket(小火箭)、v2box、v2rayn、v2rayng客户端对trojan+ws有强制开启TLS问题，造成trojan+ws不通。且clash订阅没有trojan+ws节点。特此说明


