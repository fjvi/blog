# 白嫖Cloudflare无限多企业邮箱

## 收邮件
1. 选择已绑定的域名
2. 启用email路由，选择添加4个DNS设置（3个MX，1个TXT）
3. 设置email路由规则，编辑Catch-All， 添加転送邮箱，通过邮箱验证后，状态变为可用

> [!TIP]
> 邮箱「任意@ 绑定的域名」所受到的邮件，  都会転送到Catch-All绑定的邮箱
> cloudflare邮件设置的概要栏里，可以查看所有転送的邮件


## 发邮件
通过resend.com的API服务  https://resend.com/onboarding

`Gmeek-html<img src="../imgs/resend/resend1.PNG">`
`Gmeek-html<img src="../imgs/resend/resend2.PNG">`



1. Add Domain，自动生成3条DNS（1条MX，2条TXT）
2. 添加回 cloudflare
3. 测试
```
curl -X POST 'https://api.resend.com/emails' \
 -H 'Authorization: Bearer re_123456789' \
 -H 'Content-Type: application/json' \
 -d $'{
  "from": "Acme <onboarding@resend.dev>",
  "to": ["delivered@resend.dev"],
  "subject": "hello world",
  "html": "<p>it works!</p>"
}'
```