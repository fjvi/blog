# 创建一个本地ChatGPT

### 0. 前提
本地Linux（window可以利用wsl），或者VPS上构建 Linux

### 1. 安装docker环境
```
curl -fsSL https://get.docker.com | sh    #安装Docker
systemctl enable --now docker             #启动Docker服务
docker -v                                 #查看docker版本，检查是否安装成功
```

### 2. 安装NextChat
```
docker pull yidadaa/chatgpt-next-web      #从docker拉取

docker run -d -p 3000:3000 \             #启动chatgpt-next-web
   -e OPENAI_API_KEY=sk-xxxx \
   -e CODE=页面访问密码 \
   yidadaa/chatgpt-next-web

例：docker run -d -p 3000:3000 \
   -e OPENAI_API_KEY=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 \
   -e CODE= \
   yidadaa/chatgpt-next-web
```

> [!TIP]
> 出典：https://hub.docker.com/r/yidadaa/chatgpt-next-web
> port:：3000
> OPENAI_API_KEY：通过获取 https://platform.openai.com/api-keys
> CODE：可以为空


### 3. 打开网页，即开即用
http://127.0.0.1:3000/

