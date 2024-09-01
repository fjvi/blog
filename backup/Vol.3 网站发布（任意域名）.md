```
域名　→　cloudflare　→　github
```

## 一、注册域名（任意域名）
付费的，免费的都可以，根据自身钱包的富裕程度，👀  省略若干字。。。

## 二、注册cloudflare
注册赛博大神cloudflare，利用它的DNS服务（已有账号也可以）

## 三、配置域名的NS服务
在cloudflare里选择DNS服务栏，add domain，填入域名，获取Name Serve，
复制，粘贴到域名服务商的网站，进行关联，稍等片刻cloudflare会自动check完成
`Gmeek-html<img src="https://grapehut.us.kg/imgs/cloudflare_dns.png">`

## 四、cloudflare关联github

> [!NOTE]
> IP地址  （出典：github官网）
> https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-a-subdomain

`Gmeek-html<img src="https://grapehut.us.kg/imgs/cloudflare_dns2.png">`
`Gmeek-html<img src="https://grapehut.us.kg/imgs/cloudflare_dns3.png">`

如图所示，填入IP，然后一路yes & 保存，另外SSL开启，证明书用的是默认的，


## 五、github关联域名
`Gmeek-html<img src="https://grapehut.us.kg/imgs/cloudflare_dns4.png">`

如图所示，github的custom domain里填入域名，稍等片刻后，就是见证奇迹的时刻！[小饅頭の部屋](https://grapehut.us.kg/)
至此，通过「Gmeek」构筑的超轻量级网站就诞生了。

