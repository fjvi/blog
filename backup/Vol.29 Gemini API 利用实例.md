Google Gemini 是所有一线顶级大模型当中，唯一一个 API可以免费白嫖的。
Gemini API申请：https://aistudio.google.com/apikey

1. Gemini 转OpenAI格式： https://github.com/PublicAffairs/openai-gemini
```
选择 Deploy to Cloudflare
・Account ID
・API Token  所有账户，所有区域

Fork repository

github workflower 会自动运行

最后绑定域名（例如：gemini.grapehut.us.kg）
```


2. ChatBox：https://github.com/Bin-Huang/chatbox
```
下载安装后设置
　模型提供：OPENAI API
　API         ：API密钥
　API域名  ：https://gemini.grapehut.us.kg/v1/models    ※上面第１步中指定的域名
　模型       ：自定义模型
　自定义模型名称：gemini-2.0-flash-exp

　编程模型可选：gemini exp-1206 　
```


3. Gemini多模态客户端：https://github.com/ViaAnthroposBenevolentia/gemini-2-live-api-demo
```
下载source
cd gemini-2-live-api-demo-main
cp js/config/config.example.js js/config/config.js  
Edit js/config/config.js with your API key ★ 
python -m http.server 8000
http://127.0.0.1:8000/
```


4. Worker代理：https://github.com/tech-shrimp/gemini-proxy
```
cloudflare里创建一个 worker 用于websocket-proxy （例如：gemini-proxy）
绑定域名（例如：gemini-proxy.grapehut.us.kg）
コード編集：将worker.js 的内容黏贴到 cloudflare worker
```

