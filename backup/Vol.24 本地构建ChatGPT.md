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
docker pull yidadaa/chatgpt-next-web      #从docker拉取（https://hub.docker.com/r/yidadaa/chatgpt-next-web）

docker run -d -p 3000:3000 \             #启动chatgpt-next-web
   -e OPENAI_API_KEY=sk-xxxx \
   -e CODE=页面访问密码 \
   yidadaa/chatgpt-next-web
```

> [!TIP]
> port：                    3000:3000
> OPENAI_API_KEY：通过获取 https://platform.openai.com/api-keys
> CODE：                  可以为空


### 3. 打开网页，即开即用
http://127.0.0.1:3000/

